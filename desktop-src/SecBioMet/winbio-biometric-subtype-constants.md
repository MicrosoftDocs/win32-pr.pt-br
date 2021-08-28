---
title: WINBIO_BIOMETRIC_SUBTYPE constantes (tipos \_ Winbio.h)
description: Forneça informações sobre uma medida biométrica.
ms.assetid: 019569A9-6184-4E75-9B82-C98F4F45F61A
topic_type:
- apiref
api_name:
- WINBIO_SUBTYPE_NO_INFORMATION
- WINBIO_SUBTYPE_ANY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07e6dc285e1a19fab8e0363391fbd81429e931cd
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630835"
---
# <a name="winbio_biometric_subtype-constants"></a>Constantes \_ DE \_ SUBTIPO BIOMÉTRICO WINBIO

**WINBIO \_ Constantes \_ BIOMETRIC SUBTYPE** são usadas em todo o Windows Biometric Framework para fornecer informações adicionais sobre uma medida biométrica. As constantes a seguir podem ser usadas quando nenhum subtipo é necessário ou quando qualquer subtipo é necessário.



| Constante/valor                                                                                                                                                                                                                                                            | Descrição                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span id="WINBIO_SUBTYPE_NO_INFORMATION"></span><span id="winbio_subtype_no_information"></span><dl> <dt>**WINBIO \_ SUBTIPO \_ SEM \_ INFORMAÇÕES**</dt> <dt>0X00</dt> </dl> | Nenhuma informação de subtipo.<br/> |
| <span id="WINBIO_SUBTYPE_ANY"></span><span id="winbio_subtype_any"></span><dl> <dt>**WINBIO \_ SUBTIPO \_ QUALQUER**</dt> <dt>0xFF</dt> </dl>                                   | Qualquer subtipo.<br/>            |



## <a name="remarks"></a>Comentários

Para encontrar os subtipos biométricos disponíveis para um tipo biométrico específico, use a tabela a seguir:



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th><strong>WINBIO_BIOMETRIC_TYPE</strong> valor</th>
<th>Tópicos para encontrar valores <strong>WINBIO_BIOMETRIC_SUBTYPE</strong> dados</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></td>
<td><a href="winbio-ansi-385-face-constants.md"><strong>WINBIO_ANSI_385_FACE constantes</strong></a>
<blockquote>
[!Note]<br />
Esses valores se aplicam somente a Windows 10 e posteriores.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>WINBIO_TYPE_FINGERPRINT</strong></td>
<td>Um dos seguintes tópicos:
<ul>
<li><a href="winbio-ansi-381-format-constants.md"><strong>WINBIO_ANSI_381_FORMAT constantes</strong></a></li>
<li><a href="winbio-ansi-381-img-constants.md"><strong>WINBIO_ANSI_381_IMG constantes</strong></a></li>
<li><a href="winbio-ansi-381-img-acq-constants.md"><strong>WINBIO_ANSI_381_IMG_ACQ constantes</strong></a></li>
<li><a href="winbio-ansi-381-imp-type-constants.md"><strong>WINBIO_ANSI_381_IMP_TYPE constantes</strong></a></li>
<li><a href="winbio-ansi-381-pixels-constants.md"><strong>WINBIO_ANSI_381_PIXELS constantes</strong></a></li>
<li><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>WINBIO_ANSI_381_POS constantes de impressão digital</strong></a></li>
<li><a href="winbio-ansi-381-pos-palm-constants.md"><strong>WINBIO_ANSI_381_POS_Palm constantes</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>WINBIO_TYPE_IRIS</strong></td>
<td><a href="winbio-iris-constants.md"><strong>WINBIO_IRIS constantes</strong></a>
<blockquote>
[!Note]<br />
Esses valores se aplicam somente a Windows 10 e posteriores.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>WINBIO_TYPE_VOICE</strong></td>
<td><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>WINBIO_VOICE constantes</strong></a>
<blockquote>
[!Note]<br />
Esses valores se aplicam somente a Windows 10 e posteriores.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Para obter mais informações, consulte [Constantes de aplicativo cliente](client-application-constants.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                                       |
| Cabeçalho<br/>                   | <dl> <dt>Winbio \_ types.h (inclua Winbio.h)</dt> </dl> |



 

 





