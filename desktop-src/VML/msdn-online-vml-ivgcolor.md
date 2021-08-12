---
title: IVgColor de VML
description: IVgColor de VML
ms.assetid: 6121c5bf-1969-4402-9f45-8891a1538fea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97093d9e9315db1389c71db7e8e21fdbf640353c95c5cf11f607c708e1679166
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599511"
---
# <a name="vml-ivgcolor"></a>IVgColor de VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Especifica uma cor.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributos</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>String</td>
<td>Cadeia de caracteres. Representação de texto da cor. Há suporte para os seguintes tipos de cor nomeados:
<ul>
<li>Preto (#000000)</li>
<li>Prata (#C0C0C0)</li>
<li>Cinza (#808080)</li>
<li>Branco (#FFFFFF)</li>
<li>Bordô (#800000)</li>
<li>Vermelho (#FF0000)</li>
<li>Roxo (#800080)</li>
<li>Fuchsia (#FF00FF)</li>
<li>Verde (#008000)</li>
<li>Verde-limão (#00FF00)</li>
<li>Verde-oliva (#808000)</li>
<li>Amarelo (#FFFF00)</li>
<li>Azul (#000080)</li>
<li>Azul (#0000FF)</li>
<li>Azul-petróleo (#008080)</li>
<li>Azul-piscina (#00FFFF)</li>
</ul></td>
</tr>
<tr class="even">
<td>Tipo</td>
<td>VgColorType. Tipo de cor. Um dos seguintes tipos:
<ul>
<li>Mixed</li>
<li>RGB</li>
<li>Esquema</li>
<li>nomeado</li>
</ul></td>
</tr>
<tr class="odd">
<td>RGB</td>
<td>VgRGBType. Valor RGB (<strong>Long</strong>) da cor. Somente válido se o tipo for &quot; <strong>RGB</strong> &quot; .</td>
</tr>
<tr class="even">
<td>R</td>
<td><strong>Integer</strong>. Componente vermelho da cor. Pode variar entre 0 e 255.</td>
</tr>
<tr class="odd">
<td>G</td>
<td><strong>Integer</strong>. Componente verde da cor. Pode variar entre 0 e 255.</td>
</tr>
<tr class="even">
<td>B</td>
<td><strong>Integer</strong>. Componente azul da cor. Pode variar entre 0 e 255.</td>
</tr>
</tbody>
</table>



 

 

 