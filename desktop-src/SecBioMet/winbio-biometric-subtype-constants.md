---
title: Constantes de WINBIO_BIOMETRIC_SUBTYPE (WinBio \_ Types. h)
description: Forneça informações sobre uma medição biométrica.
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
ms.openlocfilehash: ba1bc25337bf49a48b54b6b2426673daf8a15bd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918671"
---
# <a name="winbio_biometric_subtype-constants"></a>\_Constantes de SUBtipo de biometria WINBIO \_

**WINBIO \_ As constantes de \_ SUBtipo biométrica** são usadas em todo o Windows Biometric Framework para fornecer informações adicionais sobre uma medição biométrica. As constantes a seguir podem ser usadas quando nenhum subtipo é necessário ou quando qualquer subtipo é necessário.



| Constante/valor                                                                                                                                                                                                                                                            | Descrição                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span id="WINBIO_SUBTYPE_NO_INFORMATION"></span><span id="winbio_subtype_no_information"></span><dl> <dt>**WINBIO \_ Subtipo \_ nenhuma \_ informação**</dt> <dt>0x00</dt> </dl> | Nenhuma informação de subtipo.<br/> |
| <span id="WINBIO_SUBTYPE_ANY"></span><span id="winbio_subtype_any"></span><dl> <dt>**WINBIO \_ Subtipo \_ qualquer**</dt> <dt>0xFF</dt> </dl>                                   | Qualquer subtipo.<br/>            |



## <a name="remarks"></a>Comentários

Para localizar os subtipos de biometria disponíveis para um tipo biométrico específico, use a seguinte tabela:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor <strong>WINBIO_BIOMETRIC_TYPE</strong></th>
<th>Tópico (s) para localizar <strong>WINBIO_BIOMETRIC_SUBTYPE</strong> valores</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></td>
<td><a href="winbio-ansi-385-face-constants.md"><strong>WINBIO_ANSI_385_FACE constantes</strong></a>
<blockquote>
[!Note]<br />
Esses valores se aplicam somente ao Windows 10 e posterior.
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
Esses valores se aplicam somente ao Windows 10 e posterior.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>WINBIO_TYPE_VOICE</strong></td>
<td><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>WINBIO_VOICE constantes</strong></a>
<blockquote>
[!Note]<br />
Esses valores se aplicam somente ao Windows 10 e posterior.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Para obter mais informações, consulte [constantes do aplicativo cliente](client-application-constants.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



 

 





