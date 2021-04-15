---
description: Especifica informações sobre o sinal de vídeo, além do nível de proteção.
ms.assetid: ed78b7eb-bf15-4068-ab86-ae42a5e62096
title: OPM_SET_ACP_AND_CGMSA_SIGNALING (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02247c48b89e61d49afe7f8f6f3821da68ff050b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502263"
---
# <a name="opm_set_acp_and_cgmsa_signaling"></a>OPM \_ define \_ a \_ \_ sinalização ACP e CGMSA \_

Especifica informações sobre o sinal de vídeo, além do nível de proteção.



| Requisito | Valor |
|--------------|---------------------------------------------------------------------------------------------------------------------|
| GUID de comando | OPM \_ define \_ a \_ \_ sinalização ACP e CGMSA \_                                                                                |
| Dados de entrada   | Uma estrutura de [**\_ \_ \_ \_ \_ \_ parâmetros de sinalização de CGMSA**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) de dados de configuração de um OPM |



 

## <a name="remarks"></a>Comentários

Esse comando é equivalente ao comando DXVA \_ COPPSetSignaling usado no protocolo de proteção de saída certificado (Copp).

Para o CGMS-A, determinados padrões de proteção exigem que o sinal de televisão contenha informações dentro dos mesmos pacotes VBI de forma de onda que os bits CGMS-A. Entre outras coisas, essas informações incluem a taxa de proporção da imagem. As televisões podem exibir inadequadamente se as informações de taxa de proporção não estiverem consistentes com o fluxo de vídeo. O aplicativo pode usar esse comando para especificar a taxa de proporção para que o driver de gráficos possa gerar os pacotes VBI corretos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[Comandos OPM](opm-commands.md)
</dt> </dl>

 

 




