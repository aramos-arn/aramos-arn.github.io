# ⚡ Technical Ops: SysAdmin & Security
Bienvenido a mi bitácora personal. Aquí documento soluciones prácticas sobre **Administración de Sistemas**, **Arquitectura de Red** y **Hacking Ético**.

---

## 📝 Artículos Recientes

<ul>
  {% for post in site.posts %}
    <li>
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <p style="color: gray; font-size: 0.9em;">{{ post.date | date: "%d/%m/%Y" }}</p>
      <p>{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
    </li>
  {% endfor %}
</ul>

---
*Alejandro Ramos Naveros | [LinkedIn](https://www.linkedin.com/in/alex-arn/)*
