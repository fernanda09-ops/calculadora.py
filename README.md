import flet as ft

def main (page:ft.Page):

    page.title = "Calculadora"
    page.bgcolor = '#ffffff'
    page.window_center()
    page.window_width = '340'
    page.window_height = '380'
    page.window_resizable = False
    page.window_maximizable = False

    resultado_texto= ft.Text(value="0", size=28, text_align= "right")
    t= ft.Container(
        content = resultado_texto,
        bgcolor= "#d3d3d3",
        padding= 10,
        border_radius= 10,
        height= 70,
        alignment= ft.alignment.center_right

    )
    
    c1= ft.Row([
    
        ft.ElevatedButton(text="%",width=70),
        ft.ElevatedButton(text="CE",width=70),
        ft.ElevatedButton(text="C",width=70),
        ft.ElevatedButton(content=ft.Icon(ft.icons.BACKSPACE),width=70, bgcolor="#fa8f6a")
    
    ])

    c2=ft.Row([
        ft.ElevatedButton(text="7",width=70),
        ft.ElevatedButton(text="8",width=70),
        ft.ElevatedButton(text="9",width=70),
        ft.ElevatedButton(text="/",width=70, bgcolor="#fa8f6a"),

    ])

    c3=ft.Row([
        ft.ElevatedButton(text="4",width=70),
        ft.ElevatedButton(text="5",width=70),
        ft.ElevatedButton(text="6",width=70),
        ft.ElevatedButton(text="*",width=70, bgcolor="#fa8f6a"),
    ])

    c4=ft.Row([
        ft.ElevatedButton(text="1",width=70),
        ft.ElevatedButton(text="2",width=70),
        ft.ElevatedButton(text="3",width=70),
        ft.ElevatedButton(text="-",width=70, bgcolor="#fa8f6a"),
    ])

    c5=ft.Row([
        
        ft.ElevatedButton(text="0",width=70),
        ft.ElevatedButton(text=",",width=70),
        ft.ElevatedButton(text="+",width=70),
        ft.ElevatedButton(text="=",width=70, bgcolor="#fa8f6a")
    ])
        
        

    page.add(t,c1,c2,c3,c4,c5)

ft.app(target=main)
