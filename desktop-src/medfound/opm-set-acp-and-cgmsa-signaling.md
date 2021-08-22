---
description: Especifica informações sobre o sinal de vídeo, além do nível de proteção.
ms.assetid: ed78b7eb-bf15-4068-ab86-ae42a5e62096
title: OPM_SET_ACP_AND_CGMSA_SIGNALING (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 265d2986c624e30d342a4b3bc5e957e04c56bd01d51e146536de5731db42ace8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343506"
---
# <a name="opm_set_acp_and_cgmsa_signaling"></a>OPM \_ DEFINIR \_ SINALIZAÇÃO ACP \_ E \_ CGMSA \_

Especifica informações sobre o sinal de vídeo, além do nível de proteção.



| Requisito | Valor |
|--------------|---------------------------------------------------------------------------------------------------------------------|
| GUID de comando | OPM \_ DEFINIR \_ SINALIZAÇÃO ACP \_ E \_ CGMSA \_                                                                                |
| Dados de entrada   | Uma estrutura DE PARÂMETROS DE SINALIZAÇÃO [**\_ DO OPM SET ACP E \_ \_ \_ CGMSA \_ \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) |



 

## <a name="remarks"></a>Comentários

Esse comando é equivalente ao comando \_ DXVA COPPSetSignaling usado no COPP (Certified Output Protection Protocol).

Para o CGMS-A, determinados padrões de proteção exigem que o sinal de tv contenha informações dentro dos mesmos pacotes de forma de onda da VBI que os bits CGMS-A. Entre outras coisas, essas informações incluem a taxa de proporção da imagem. Os programas de tv poderão ser exibidos incorretamente se as informações da taxa de proporção não são consistentes com o fluxo de vídeo. O aplicativo pode usar esse comando para especificar a taxa de proporção para que o driver gráfico possa gerar os pacotes de VBI corretos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[Comandos do OPM](opm-commands.md)
</dt> </dl>

 

 




