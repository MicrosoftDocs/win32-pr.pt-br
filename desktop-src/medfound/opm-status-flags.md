---
description: Os sinalizadores na tabela a seguir especificam o status de uma sessão do Gerenciador de proteção de saída (OPM).
ms.assetid: d6d85fd4-e735-4610-93e0-bb2b1782f11b
title: Sinalizadores de status OPM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edc044d9159ad6e6a6e957c4be0228a8e2531164
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480192"
---
# <a name="opm-status-flags"></a>Sinalizadores de status OPM

Os sinalizadores na tabela a seguir especificam o status de uma sessão do Gerenciador de proteção de saída (OPM).




| Constante/valor | Descrição | 
|----------------|-------------|
| <span id="OPM_STATUS_NORMAL"></span><span id="opm_status_normal"></span><dl><dt><strong>OPM_STATUS_NORMAL</strong></dt><dt>0x00</dt></dl> | Status normal.<br /> | 
| <span id="OPM_STATUS_LINK_LOST"></span><span id="opm_status_link_lost"></span><dl><dt><strong>OPM_STATUS_LINK_LOST</strong></dt><dt>0x01</dt></dl> | A integridade da conexão foi comprometida. Exemplos de eventos que fazem com que o driver defina esse sinalizador incluem:<br /><ul><li>O driver não pode mais impor o nível de proteção atual.</li><li>O driver detectou um erro de integridade interno.</li><li>O conector entre o computador e o dispositivo de vídeo foi desconectado.</li></ul> | 
| <span id="OPM_STATUS_RENEGOTIATION_REQUIRED"></span><span id="opm_status_renegotiation_required"></span><dl><dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt><dt>0x02</dt></dl> | A configuração de conexão foi alterada. Por exemplo, o usuário alterou o modo de exibição da área de trabalho.<br /> | 
| <span id="OPM_STATUS_TAMPERING_DETECTED"></span><span id="opm_status_tampering_detected"></span><dl><dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt><dt>0x04</dt></dl> | O adaptador gráfico ou o driver foi adulterado.<br /> Esse sinalizador não é usado no <em>modo de emulação Copp</em>. Em vez disso, a saída de vídeo definirá o sinalizador OPM_STATUS_LINK_LOST se detectar violação.<br /> | 
| <span id="OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED"></span><span id="opm_status_revoked_hdcp_device_attached"></span><dl><dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt><dt>0x08</dt></dl> | Um dispositivo de Proteção de Conteúdo Digital High-Bandwidth revogado (HDCP) é anexado à saída de vídeo.<br /> Esse sinalizador de status pode ser retornado de uma consulta <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> ou <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> . <br /> O dispositivo revogado pode ser anexado diretamente à saída de vídeo ou indiretamente por meio de um repetidor HDCP. Uma saída de vídeo é necessária para detectar essa condição enquanto a HDCP está habilitada, mas não de outra forma.<br /> Esse sinalizador não é usado no <em>modo de emulação de Copp</em>, pois a saída de vídeo não detecta dispositivos revogados nesse modo.<br /> | 




## <a name="remarks"></a>Comentários

Algumas dessas constantes são equivalentes aos valores da enumeração **Copp \_ StatusFlags** usada no protocolo de proteção de saída certificado (Copp).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações de OPM](opm-enumerations.md)
</dt> </dl>

 

 




