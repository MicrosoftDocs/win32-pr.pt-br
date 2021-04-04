---
title: Constantes de WINBIO_CAPABILITY (WinBio \_ Types. h)
description: Subtipos de sensor de impressão digital.
ms.assetid: D447273E-2A02-484E-B0E4-69FEADD15797
topic_type:
- apiref
api_name:
- WINBIO_CAPABILITY_SENSOR
- WINBIO_CAPABILITY_MATCHING
- WINBIO_CAPABILITY_DATABASE
- WINBIO_CAPABILITY_PROCESSING
- WINBIO_CAPABILITY_ENCRYPTION
- WINBIO_CAPABILITY_NAVIGATION
- WINBIO_CAPABILITY_INDICATOR
- WINBIO_CAPABILITY_VIRTUAL_SENSOR
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f16de3f496e5c3723722bb7aae22c81eb27c968
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824432"
---
# <a name="winbio_capability-constants"></a>\_Constantes de recurso WINBIO

Os seguintes subtipos de sensor de impressão digital são valores de **\_ recursos WINBIO** que podem ser usados como bitmask para o parâmetro *Capabilities* da estrutura de [**\_ \_ esquema de unidade WINBIO**](winbio-unit-schema.md) . Eles se referem aos recursos do sensor integrado.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante/valor</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_SENSOR"></span><span id="winbio_capability_sensor"></span><dl> <dt><strong>WINBIO_CAPABILITY_SENSOR</strong></dt> <dt>0x00000001</dt> </dl></td>
<td style="text-align: left;">O sensor pode capturar dados biométricos.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_MATCHING"></span><span id="winbio_capability_matching"></span><dl> <dt><strong>WINBIO_CAPABILITY_MATCHING</strong></dt> <dt>0x00000002</dt> </dl></td>
<td style="text-align: left;">O sensor pode corresponder dados biométricos a uma identidade.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_DATABASE"></span><span id="winbio_capability_database"></span><dl> <dt><strong>WINBIO_CAPABILITY_DATABASE</strong></dt> <dt>0x00000004</dt> </dl></td>
<td style="text-align: left;">O sensor contém um banco de dados integrado.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_PROCESSING"></span><span id="winbio_capability_processing"></span><dl> <dt><strong>WINBIO_CAPABILITY_PROCESSING</strong></dt> <dt>0x00000008</dt> </dl></td>
<td style="text-align: left;">O sensor pode executar o processamento biométrico.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_ENCRYPTION"></span><span id="winbio_capability_encryption"></span><dl> <dt><strong>WINBIO_CAPABILITY_ENCRYPTION</strong></dt> <dt>0x00000010</dt> </dl></td>
<td style="text-align: left;">O sensor pode criptografar dados biométricos.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_NAVIGATION"></span><span id="winbio_capability_navigation"></span><dl> <dt><strong>WINBIO_CAPABILITY_NAVIGATION</strong></dt> <dt>0x00000020</dt> </dl></td>
<td style="text-align: left;">O sensor pode atuar como um mouse pad. Não há suporte para esse recurso no momento.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_INDICATOR"></span><span id="winbio_capability_indicator"></span><dl> <dt><strong>WINBIO_CAPABILITY_INDICATOR</strong></dt> <dt>0x00000040</dt> </dl></td>
<td style="text-align: left;">O sensor contém uma luz do indicador.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_VIRTUAL_SENSOR"></span><span id="winbio_capability_virtual_sensor"></span><dl> <dt><strong>WINBIO_CAPABILITY_VIRTUAL_SENSOR</strong></dt> <dt>0x00000080</dt> </dl></td>
<td style="text-align: left;">O adaptador do sensor gerencia sua própria conexão com o hardware biométrico.<br/>
<blockquote>
[!Note]<br />
Essa constante se aplica somente ao Windows 10 e posterior.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                                                                                  |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de aplicativo cliente](client-application-constants.md)
</dt> <dt>

[**\_esquema de unidade WINBIO \_**](winbio-unit-schema.md)
</dt> </dl>

 

 





