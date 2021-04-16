---
description: Os sinalizadores na tabela a seguir especificam o status de uma sessão do Gerenciador de proteção de saída (OPM).
ms.assetid: d6d85fd4-e735-4610-93e0-bb2b1782f11b
title: Sinalizadores de status OPM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cbf9d299d6d53a26a61d19372e56e42bd2cdf99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502262"
---
# <a name="opm-status-flags"></a>Sinalizadores de status OPM

Os sinalizadores na tabela a seguir especificam o status de uma sessão do Gerenciador de proteção de saída (OPM).



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
<td style="text-align: left;"><span id="OPM_STATUS_NORMAL"></span><span id="opm_status_normal"></span><dl> <dt><strong>OPM_STATUS_NORMAL</strong></dt> <dt>0x00</dt> </dl></td>
<td style="text-align: left;">Status normal.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_LINK_LOST"></span><span id="opm_status_link_lost"></span><dl> <dt><strong>OPM_STATUS_LINK_LOST</strong></dt> <dt>0x01</dt> </dl></td>
<td style="text-align: left;">A integridade da conexão foi comprometida. Exemplos de eventos que fazem com que o driver defina esse sinalizador incluem:<br/>
<ul>
<li>O driver não pode mais impor o nível de proteção atual.</li>
<li>O driver detectou um erro de integridade interno.</li>
<li>O conector entre o computador e o dispositivo de vídeo foi desconectado.</li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_RENEGOTIATION_REQUIRED"></span><span id="opm_status_renegotiation_required"></span><dl> <dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt> <dt>0x02</dt> </dl></td>
<td style="text-align: left;">A configuração de conexão foi alterada. Por exemplo, o usuário alterou o modo de exibição da área de trabalho.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_TAMPERING_DETECTED"></span><span id="opm_status_tampering_detected"></span><dl> <dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt> <dt>0x04</dt> </dl></td>
<td style="text-align: left;">O adaptador gráfico ou o driver foi adulterado.<br/> Esse sinalizador não é usado no <em>modo de emulação Copp</em>. Em vez disso, a saída de vídeo definirá o sinalizador OPM_STATUS_LINK_LOST se detectar violação.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED"></span><span id="opm_status_revoked_hdcp_device_attached"></span><dl> <dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt> <dt>0x08</dt> </dl></td>
<td style="text-align: left;">Um dispositivo de Proteção de Conteúdo Digital High-Bandwidth revogado (HDCP) é anexado à saída de vídeo.<br/> Esse sinalizador de status pode ser retornado de uma consulta <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> ou <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> . <br/> O dispositivo revogado pode ser anexado diretamente à saída de vídeo ou indiretamente por meio de um repetidor HDCP. Uma saída de vídeo é necessária para detectar essa condição enquanto a HDCP está habilitada, mas não de outra forma.<br/> Esse sinalizador não é usado no <em>modo de emulação de Copp</em>, pois a saída de vídeo não detecta dispositivos revogados nesse modo.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Comentários

Algumas dessas constantes são equivalentes aos valores da enumeração **Copp \_ StatusFlags** usada no protocolo de proteção de saída certificado (Copp).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações de OPM](opm-enumerations.md)
</dt> </dl>

 

 




