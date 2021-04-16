---
title: Estilos estendidos de controle de edição (CommCtrl. h)
description: Esta seção lista os estilos estendidos usados ao criar controles de edição. O valor dos estilos estendidos é uma combinação bit-a-bit desses estilos.
ms.assetid: 44ef7cbf-6d90-4ea0-8e23-cd84aacd5506
topic_type:
- apiref
api_name:
- ES_EX_ALLOWEOL_CR
- ES_EX_ALLOWEOL_LF
- ES_EX_ALLOWEOL_ALL
- ES_EX_CONVERT_EOL_ON_PASTE
- ES_EX_ZOOMABLE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 912a13b0e05d7b12e5058435221b821b50eddf2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750550"
---
# <a name="edit-control-extended-styles"></a>Editar estilos estendidos de controle

Esta seção lista os estilos estendidos usados ao criar controles de edição. O valor dos estilos estendidos é uma combinação bit-a-bit desses estilos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ES_EX_ALLOWEOL_CR"></span><span id="es_ex_alloweol_cr"></span><dl> <dt><strong>ES_EX_ALLOWEOL_CR</strong></dt> </dl></td>
<td style="text-align: left;">[Windows Vista e posterior](common-control-versions.md). Habilita o suporte para caracteres de término de retorno de carro (CR) para quebra de linha.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_EX_ALLOWEOL_LF"></span><span id="es_ex_alloweol_lf"></span><dl> <dt><strong>ES_EX_ALLOWEOL_LF</strong></dt> </dl></td>
<td style="text-align: left;">[Windows Vista e posterior](common-control-versions.md). Habilita o suporte para caracteres de finalização de linhagem (LF) para quebrar linhas.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_EX_ALLOWEOL_ALL"></span><span id="es_ex_alloweol_all"></span><dl> <dt><strong>ES_EX_ALLOWEOL_ALL</strong></dt> </dl></td>
<td style="text-align: left;">[Windows Vista e posterior](common-control-versions.md). Habilita o suporte para caracteres de fim de retorno de carro (CR) e alimentação de linha (LF) para quebrar linhas.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_EX_CONVERT_EOL_ON_PASTE"></span><span id="es_ex_convert_eol_on_paste"></span><dl> <dt><strong>ES_EX_CONVERT_EOL_ON_PASTE</strong></dt> </dl></td>
<td style="text-align: left;">[Windows Vista e posterior](common-control-versions.md). Converte os caracteres de fim de linha habilitados para este controle de edição no conteúdo colado para corresponder ao caractere de fim de linha usado pelo documento atual.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_EX_ZOOMABLE"></span><span id="es_ex_zoomable"></span><dl> <dt><strong>ES_EX_ZOOMABLE</strong></dt> </dl></td>
<td style="text-align: left;">[Windows Vista e posterior](common-control-versions.md). Permite o zoom usando Ctrl + MouseWheel e as mensagens em [**\_ getzoom**](em-getzoom.md)em / [**\_ setZoom**](em-setzoom.md) .<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





