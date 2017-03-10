---
layout: default
intro: 'Artículo acerca de las cerificaciones AWS'
title: Cómo aprobar las certificaciones AWS
category: linux
meta_contenido: certificaciones aws
date: 2017-03-10T12:05:00Z
---

<h1 class="centrar-titulo-blog">Cómo aprobar las certificaciones AWS</h1>

<p><em>Traducción del artículo de Adrian Cantrill (<a href="https://twitter.com/adriancantrill">@adriancantrill</a>) publicado originalmente el 27 de marzo de 2016 como “<strong>How to pass AWS certifications</strong>”
en <a href="http://cantrill.io/certification/aws/2016/03/27/how-to-pass-AWS-certifications.html">http://cantrill.io/certification/aws/2016/03/27/how-to-pass-AWS-certifications.html</a></em></p>

Mar 27, 2016 • Adrian Cantrill

He estado trabajando con AWS por más de siete años y el año pasado (2015) aprobé mi último examen AWS uniéndome así a un grupo pequeño de personas que han alcanzado 5 de 5 certificaciones. Aparte de eso, soy un auto confeso adicto a las certificaciones y desde hace poco un entrenador online después de haber sido coautor de un curso para Ingeniero DevOps certificado de AWS ⎼ nivel profesional con Nick Triantafillou.

Aprobé todos los cinco exámenes en menos de un año y eso incluyendo un descanso de seis meses. Una de las preguntas que me hacen con frecuencia es ¿Cómo lo hice? ¿Yuve algún método y qué material usé? Esta publicación tiene la intención de brindar esa información pero enfocándose en lo que se necesita para **aprobar** el examen.

<h2 class="blog-h2">La estructura de la certificación AWS</h2>

AWS tiene actualmente tres niveles básicos de certificaciones:
1. Arquitectura de Soluciones ⎼ Nivel Asociado
2. Desarrollador ⎼ Nivel Asociado
3. Administrador SysOps ⎼ Nivel Asociado

El examen de arquitecto de soluciones evalúa la habilidad de desarrollar soluciones a nivel básico. Usted tendrá que entender el conjunto de características básicas ofrecido por por la mayoría de los servicios principales de AWS y tener la habilidad de criticar diseños de otros. Usted deberá entender los elementos, límites y temas específicos principales de los servicios básicos de AWS. No deje que el término desarrollador le incomode, usted no tendrá necesidad de programar para aprobar este examen, pero le será necesario entender el CLI y algunos llamados a la API más utilizados y de alto nivel. Además, deberá tener una comprensión sólida de dynamoDB y SQS. Finalmente, tenemos la certificación de Administrador SysOps, el examen que en mi opinión es **de lejos** el más difícil de las certificaciones de nivel asociado. Este examen evaluará su habilidad de implementar, administrar y detectar fallas en todos los servicios AWS fundamentales cubiertos por los otros dos exámenes. Se esperará que usted conozca la implementación y gestión de elementos de los servicios junto con características claves de límites y desempeño de servicios. En este examen más que en los otros dos se espera que usted haya **usado** y **manejado** los servicios de AWS en casos reales. Todos los exámenes de nivel asociado tiene 40 preguntas y usted tiene 90 minutos para completarlos.

Las certificaciones de nivel profesional son un **gran** paso adelante  con respecto al nivel asociado, y esto tengo que subrayarlo muy bien, son **muy** exigentes; y se espera una experiencia detallada y profunda de una serie más amplia de servicios AWS. Actualmente hay dos exámenes de nivel profesional:

1. Arquitecto de soluciones ⎼ Profesional
2. Ingeniero DevOps ⎼ Profesional

Cada examen es más extenso, 80 preguntas y 180 minutos. Los exámenes requieren haber completado las certificaciones de nivel asociado primero. En el primer caso, el arquitecto de soluciones profesional exige el arquitecto de soluciones asociado; el DevOps profesional necesita el desarrollador o SysOps asociado antes de inscribirse.

<h2 class="blog-h2">El orden que seguí, los temas que se superponen y el orden sugerido</h2>

A menudo me preguntan qué secuencia escogí para estudiar y tomar los exámenes y si tengo algún hechizo para las certificaciones AWS que pueda compartir. No es magia pero hay un cierto orden y formato que veo como óptimo y eficiente. Primero, veamos los esquemas para las certificaciones
[Arquitecto de Soluciones Asociado](https://d0.awsstatic.com/training-and-certification/docs-sa-assoc/AWS_certified_solutions_architect_associate_blueprint.pdf), [Desarrollador Asociado](http://awstrainingandcertification.s3.amazonaws.com/production/AWS_certified_developer_associate_blueprint.pdf) y [Administrador SysOps Asociado](http://awstrainingandcertification.s3.amazonaws.com/production/AWS_certified_sysops_associate_blueprint.pdf). Lo primero que debería ser evidente es que hay un gran superposición de temas en los certificados arquitecto de soluciones asociado y desarrollador asociado. Mi consejo para los estudiantes siempre ha sido que estudien para el arquitecto de soluciones primero, asegurándose de de cubrir la totalidad del contenido del examen. Cuando esté seguro de sí mismo, inscríbase y ojalá pase el examen. Suponiendo que le fue bien, estudie DynamoDB y SQS en detalle y usted encontrará que muchos de los otros temas ya han sido cubiertos por el examen de arquitecto de soluciones. Ahora usted debería estar listo para para tomar y aprobar la certificación de desarrollador bastante rápidamente luego del AS asociado, en mi caso esto ocurrió en menos de 10 días luego de mi primer examen. Casi todo el mundo al que le doy este consejo lo ignora y después me dicen que ojalá no lo hubieran ignorado. Tómalo o déjalo pero yo sostengo que este es el método más eficiente para una aprobación de examen 2 por 1. En este punto, usted ya debería poseer ⅔ de las certificaciones de nivel asociado y ahora se puede enfocar en la certificación administrador SysOps que en mi opinión es la más difícil en este nivel y con la menor cantidad de temas superpuestos.

En el nivel profesional las cosas *llegan a lo más alto*. Debido a la amplitud y profundidad del conocimiento exigido no hay un método sencillo para completarlos. Mi sugerencia podría ser dejar un espacio entre las certificaciones de nivel asociado y profesional; con suerte usted está usando AWS profesionalmente, si no, trabaje duro para adquirir experiencia práctica. Ya le voy a dar unos tips más adelante, pero no subestime la cantidad de conocimiento necesario para el nivel profesional.

Personalmente yo combiné el estudio de ambos. Había cierto nivel de superposición y encontré útil estar sumergido en el material de estudio más general. Estudié por cerca de dos meses cubriendo el material de ambas certificaciones. Tomé el el arquitecto de soluciones profesional, lo aprobé, y continué con el examen DevOps profesional dos semanas después. Yo no le recomendaría a nadie que siguiera este enfoque. Usted necesitaría un jefe y cónyuge muy comprensivos, pero es ciertamente posible de realizar. Usted es la única persona que puede juzgar el progreso hecho con relación al esfuerzo invertido.

<h2 class="blog-h2">Consígase una cuenta AWS y úsela!!</h2>

Esto hay que señalarlo verdaderamente; muchos de los cursos de entrenamiento online (incluido el que yo ayudé a crear) están basados en la teoría. Le dan a usted el conocimiento detallado de la configuración del producto, de casos reales de uso y arquitecturas; pero ellos confían en que usted invierta una considerable cantidad de tiempo en las herramientas reales tanto GUI como CLI. AWS ofrece un modelo de cobro por horas a la vez que un generosa [capa gratuita (free tier)](https://aws.amazon.com/free/?tag=vig-20) con los que se pueden probar varios servicios sin costo. Mi consejo es que cree una cuenta en la [consola de AWS](https://aws.amazon.com/es/?nc1=h_ls) y comience a probar todos los servicios disponibles. Tenga muy en cuenta las disposiciones de la capa gratuita de modo que no vaya a tener sorpresas desagradables.

En el nivel asociado le puede bastar en la mayoría de los casos con una comprensión del GUI para acceso a los servicios. En nivel profesional, le será necesario conocer el GUI, CLI y la API con mucho detalle.

<h2 class="blog-h2">Entrenamiento Online</h2>

(*Advertencia: soy productor de contenido para el grupo en A Cloud Guru, pero también he usado sus recursos en mis estudios. Estoy tratando de ser imparcial, pero tenga en cuenta la circunstancia...*)

Hay cuatro principales fuentes de entrenamiento online en temas AWS. A [Cloud Guru](https://acloud.guru/), [Udemy](https://www.udemy.com/courses/), [LinuxAcademy](https://linuxacademy.com/) y [Cloud Academy](https://cloudacademy.com/). Agregué *Udemy* pero ellos realmente son revendedores de contenido de creadores independientes incluyendo *Cloud Guru* y *LinuxAcademy*. También agregué a *Cloud Academy* para ser exhaustivo pero yo me mantendría 100% **alejado** de su contenido. He visto que no solo su calidad deja mucho que desear sino que la información es a menudo incorrecta y tiene explicaciones mal escritas; creo que es más perjudicial que ventajoso a la hora de estudiar.

Eso deja a **A Cloud Guru** y **LinuxAcademy**. Ambos ofrecen cursos de certificación para los tres cursos de nivel asociado y de arquitecto de soluciones profesional, pero hasta ahora A Cloud Guru es el único que ofrece el curso de entrenamiento de
[Ingeniero DevOps](https://acloud.guru/login?backUrl=%2Fcourses&successUrl=%2Fcourse%2Faws-certified-devops-engineer-professional%2Fdashboard&loginCategory=course) (cuyo coautor es este servidor).

Con A Cloud Guru (ACG) y LinuxAcademy (LA) la selección es bastante sencilla. Con ACG usted compra los cursos y son suyos de por vida. Con LA usted paga una suscripción y alquila el contenido; si usted deja de pagar bien sea intencionalmente o por otras razones, usted no puede acceder al contenido. Además, los cursos ACG están **considerablemente** optimizados y diseñados para que usted adquiera el conocimiento necesario para aprobar el examen tan rápido y eficientemente como sea posible. Si usted valora la eficiencia y el énfasis en su estudio de certificación, entonces ACG es el equipo para usted. Son un grupo de personas muy cualificadas y la principal razón por la que decidí asociarme con ellos en el lanzamiento del curso de Ingeniero DevOps Profesional.

Cuando comencé había un limitado número de cursos online disponibles, pero he estado recomendando ACG a mis colegas y amigos durante el último año y todos han reaccionado de forma favorable. Mi sugerencia es que usted elija o los cursos individuales o los paquetes disponibles [aquí](https://acloud.guru/courses).

<h2 class="blog-h2">Recursos Online</h2>

Aparte de los cursos mencionados arriba, existen algunos recursos online que he recomendado a compañeros de trabajo y amigos durante su esfuerzo de certificación.

Primero, he creado un cierto número de publicaciones de blog que dan recomendaciones de las certificaciones del nivel profesional, uno para el [Arquitecto de Soluciones Profesional](http://cantrill.io/certification/aws/2015/10/04/passing-the-aws-solutions-architect-professional-exam.html) y el otro para el [Ingeniero DevOps Profesional](http://cantrill.io/certification/aws/2015/10/29/passing-the-aws-devops-engineer-professional-exam.html). Mi coautor y colega, [Nick](https://twitter.com/xelfer) también ha escrito un par de entradas, también para el Arquitecto de Soluciones Profesional y la otra para el Ingeniero DevOps Profesional.


Además de estos, también recomendaría ver el canal de AWS en Youtube prestando bastante atención a las sesiones de entrenamiento y de Amazon re-invent. La mayoría de los videos siguen el formato 1XX, 2XX, 3XX y 4XX, cada uno de los cuales aumenta la dificultad. Para las certificaciones de nivel asociado yo comenzaría con los videos 2XX y luego seguiría con 3XX y 4XX del nivel profesional

Mientras se estudia, sería bueno estar pendiente de los [blogs](https://aws.amazon.com/es/blogs/aws/?tag=vig-20) acerca de AWS, específicamente en las áreas de Arquitectura, Seguridad y Computación. Todos ellos contienen artículos muy bien documentados que van a ayudar en el estudio y el examen.

<h2 class="blog-h2">Converse con personas que ya lo han presentado</h2>

Mientras yo estudiaba, no había mucho material aparte de la documentación oficial de AWS. Actualmente, hay un número creciente de personas que han completado 3 de 5 o 5 de 5 exámenes muchos de los cuales han escrito entradas de blog o están presentes en comunidades como [AWS Sub-Reddit](https://www.reddit.com/r/aws/) o los foros de discusión de Cloud Guru. El equipo de Cloud Guru, incluido [Ryan Kroonenburg](https://twitter.com/kroonenburgryan), revisan regularmente los foros y contestan las preguntas que se hacen. Nick, mi persona y muchos otros ingenieros y consultores AWS leen, escriben y responden regularmente en AWS Sub-Reddit. Así es que  si usted tiene preguntas ése es el lugar para consultar. Ante todo, involúcrese; usted no está en este proceso solo y hay consejos valiosos que recibir y discusiones en las que participar.

<h2 class="blog-h2">Consígase un compañero de estudio</h2>

No puedo resaltar lo suficiente la importancia de tener uno o más compañeros de estudio mientras se preparan para las certificaciones. Yo lo hice con las certificaciones de nivel asociado con un grupo de amigos con los que trabajaba y fuimos capaces de mantener a cada uno motivado a través de apoyo mutuo y sana competición. Terminamos no solo obteniendo buenos resultados, sino también obteniendo los certificados más rápido de lo que generalmente se espera.

Para las certificaciones de nivel profesional intente encontrar a alguien que sean tan dedicado como usted. El camino para obtener el nivel PRO es más largo y más exigente que para los niveles básicos, de modo que va a ayudar inmensamente tener a alguien con quien hacerlo. Yo completé el arquitecto de soluciones profesional con un colega y mi DevOps profesional con Nick. Ustedes pueden evaluarse entre sí con preguntas y brindar ideas y respuestas alternativas en los exámenes de práctica. Una opción es ir a Reddit o a los foros de Cloud Guru a ver si alguien quiere trabajar con usted online para crear un grupo de estudio.

<h2 class="blog-h2">Práctica</h2>

AWS ofrece [exámenes de práctica](https://www.webassessor.com/wa.do?page=publicHome&branding=AMAZON) para todas las certificaciones. Además, se pueden descargar y ver ejemplos de preguntas en los enlaces a continuación.

1. Arquitecto de Soluciones Asociado ([AQUÍ](http://awstrainingandcertification.s3.amazonaws.com/production/AWS_certified_solutions_architect_associate_examsample.pdf))
2. Desarrollador ([AQUÍ](http://awstrainingandcertification.s3.amazonaws.com/production/AWS_certified_developer_associate_examsample.pdf))
3. Administración SysOps ([AQUÍ](http://awstrainingandcertification.s3.amazonaws.com/production/AWS_certified_sysops_associate_examsample.pdf))
4. Arquitecto de Soluciones Profesional ([AQUÍ](https://d0.awsstatic.com/Train%20&%20Cert/docs/AWS_certified_solutions_architect_professional_examsample.pdf))
5. Ingeniero DevOps ([AQUÍ](https://d0.awsstatic.com/training-and-certification/docs/AWS_certified_DevOps_Engineer_Professional_SampleExam.pdf))

<h2 class="blog-h2">El día del examen</h2>

Se debe intentar presentar máximo un examen al día. He escuchado de personas que han tratado de pasar varios exámenes el mismo día luego de estudiar para ambos, pero me han ocurrido problemas con terminales dañadas en el centro examinador o retrasos debido a problemas de electricidad o ensayos de evacuación incendio. Es más seguro y menos estresante limitarse a uno por día.

Hay que llegar al centro evaluador temprano y no olvidar el código de acceso que se recibe cuando uno se inscribe para el examen. El centro de certificación no tiene acceso directo a éste, de modo que no se debe olvidar. También se necesitan dos tipos de identificación, una con una foto y otra con la firma; los pasaportes, licencias de conducción o tarjetas de crédito son ideales para eso.

El proceso de ingreso y validación toma entre cinco y quince minutos dependiendo de si se ha estado en el centro de certificación antes. Hay que asegurarse de tener tiempo suficiente. No es deseable tener que estar corriendo durante el examen.

No se permite ingresar ningún tipo de material al salón ni tampoco se permite salir del examen sin acompañamiento luego de que el test comienza. Asegúrese de hacer una parada por el baño con anticipación. La mayoría de los centros examinadores brindan lockers para las cosas valiosas.

Por encima de todo, asegúrese de estar preparado y el examen será una experiencia normal. Mi experiencia fue que al final de los exámenes de nivel asociado me sobró mucho tiempo, pero me sentí presionado con el tiempo en los tests de nivel profesional.

En el nivel asociado se tienen 40 preguntas y 90 minutos para completarlas. Las preguntas son de 1-3 líneas de extensión y generalmente tiene cuatro opciones, cada una de una línea. Hay que asegurarse de tomarse el tiempo de leer y responder cada una con cuidado. Existe la opción de marcar las respuestas para revisarlas posteriormente. Yo respondería sólo las que me siento seguro que sé y regresaría a aquellas cuya respuesta está en duda. Se tiende a cometer menos errores cuando uno no se siente tan apremiado.

Los exámenes de nivel profesional son mucho más difíciles. Se tienen 80 preguntas y 180 minutos para completar el examen. Pero las preguntas son más largas, tienen entre cinco y diez líneas con opciones de tres y cuatro líneas cada una. Las preguntas son mucho más complejas y evalúan tanto la comprensión como el conocimiento técnico. Además, en el nivel asociado para cada pregunta se tiene una respuesta correcta, una posible y dos erroneas. En el nivel profesional generalmente se tienen múltiples respuestas correctas y se pide escoger la más apropiada. Hay que ir a los exámenes de ambos niveles con seguridad. Si no se está nervioso y no se tiene que adivinar, el desempeño general va a ser mucho mejor con el tiempo disponible.

<h2 class="blog-h2">Aquí estoy si soy de alguna ayuda…</h2>

Bien, eso es todo lo que iba a decir, si usted tiene preguntas específicas, déjelas en los comentarios abajo o en los foros de Cloud Guru y haré lo mejor por responder.

Si tiene preguntas o comentarios, publíquelas a continuación. Si le gustó la publicación, puede compartirla con sus seguidores o [seguirme en Twitter](https://twitter.com/adriancantrill)!
