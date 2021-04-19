---
description: Especifica como a sessão de mídia desliga um objeto na topologia.
ms.assetid: 53b4faba-860f-4d6c-a145-09ea4ae63b8b
title: Atributo MF_TOPONODE_NOSHUTDOWN_ON_REMOVE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bec06d2190491167d978250270503e5e6506d58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105786182"
---
# <a name="mf_toponode_noshutdown_on_remove-attribute"></a>MF \_ TOPONODE \_ parashutdown \_ no \_ atributo remove

Especifica como a sessão de mídia desliga um objeto na topologia.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Tratar como um valor booliano.

## <a name="remarks"></a>Comentários

Esse atributo se aplica aos seguintes tipos de nó topologia:

-   Nós de saída
-   Qualquer nó de transformação que contenha uma Media Foundation de transformação *assíncrona* (MFT).

O atributo pode ter os seguintes valores:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>TRUE</strong></td>
<td>Quando a sessão de mídia alterna para uma nova topologia ou limpa a topologia atual, ela não encerra o objeto que pertence a esse nó de topologia.</td>
</tr>
<tr class="even">
<td><strong>FALSE</strong></td>
<td>Quando a sessão de mídia alterna para uma nova topologia ou limpa a topologia atual, ela desliga o objeto de nó, da seguinte maneira:
<ul>
<li>Nós de saída: a sessão chama <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown"><strong>IMFMediaSink:: Shutdown</strong></a> no coletor de mídia.</li>
<li>Nós de transformação: a sessão chama <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown"><strong>IMFShutdown:: Shutdown</strong></a> no MFT.</li>
</ul></td>
</tr>
</tbody>
</table>



 

O valor padrão é **true**.

Se o seu aplicativo enfileira várias topologias, é uma boa ideia definir esse atributo como **false**. Caso contrário, os objetos na topologia podem não ser desligados corretamente.

Esse atributo não se aplica quando o aplicativo desliga a sessão de mídia chamando [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown). Quando a sessão de mídia é desligada, ela sempre desliga os coletores de mídia e MFTs assíncronas na topologia atual.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs assíncrona](asynchronous-mfts.md)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




