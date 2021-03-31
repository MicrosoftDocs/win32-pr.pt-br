---
description: No Microsoft Media Foundation, uma fila de trabalho é uma maneira eficiente de executar operações assíncronas em outro thread.
ms.assetid: f886d096-b1f5-42e4-8888-501b58bffd50
title: Filas de trabalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b1e5e8a0a3776f718f645550813bf008b38aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169752"
---
# <a name="work-queues"></a>Filas de trabalho

No Microsoft Media Foundation, uma fila de trabalho é uma maneira eficiente de executar operações assíncronas em outro thread.

Esta seção contém os seguintes tópicos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tópico</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="using-work-queues.md">Usando filas de trabalho</a></td>
<td>Descreve como um aplicativo ou componente pode usar filas de trabalho para executar operações assíncronas.</td>
</tr>
<tr class="even">
<td><a href="writing-an-asynchronous-method.md">Escrevendo um método assíncrono</a></td>
<td>Descreve como escrever um método assíncrono que segue o padrão de início/término descrito em <a href="asynchronous-callback-methods.md">métodos de retorno de chamada assíncronos</a>.</td>
</tr>
<tr class="odd">
<td><a href="custom-asynchronous-result-objects.md">Objetos de resultados assíncronos personalizados</a></td>
<td>Descreve como criar uma implementação personalizada da interface <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult"><strong>IMFAsyncResult</strong></a> .<br/>
<blockquote>
[!Note]<br />
A maioria dos aplicativos deve usar a implementação de estoque fornecida pelo <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult"><strong>MFCreateAsyncResult</strong></a>. Este tópico é para aplicativos com requisitos avançados.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="media-foundation-work-queue-and-threading-improvements.md">Aprimoramentos na fila de trabalho e threading</a></td>
<td>Descreve melhorias no Windows 8 para filas de trabalho e threading na plataforma Media Foundation.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[APIs da plataforma Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 




