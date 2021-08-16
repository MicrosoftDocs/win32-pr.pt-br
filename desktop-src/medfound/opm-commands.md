---
description: Comandos do OPM
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: Comandos do OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f6d21119f86ab8f51392df248498681f8fe5dc1aa8218a0232b9f3bd1c7cb02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722236"
---
# <a name="opm-commands"></a>Comandos do OPM

Esta seção lista os comandos disponíveis para o [OPM (Gerenciador de Proteção de Saída).](output-protection-manager.md)

Para enviar um comando OPM, chame [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure). Para cada comando, as informações a seguir são listadas.



| Valor             | Descrição                                                                                                                                                            |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de comando | Identifica o comando . De definir **o membro guidSetting** da estrutura [**CONFIGURE \_ \_ PARAMETERS do OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) igual a esse valor. |
| Dados de entrada   | Especifica como interpretar a **matriz abParameters** na estrutura [**CONFIGURE \_ \_ PARAMETERS do OPM.**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters)                      |



 

Os seguintes comandos são definidos:



| Comando                                                                                                       | Descrição                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**OPM \_ DEFINIR \_ SINALIZAÇÃO ACP \_ E \_ CGMSA \_**](opm-set-acp-and-cgmsa-signaling.md)                               | Especifica informações sobre o sinal de vídeo, além do nível de proteção.                      |
| [**OPM \_ SET \_ HDCP \_ SRM**](opm-set-hdcp-srm.md)                                                               | Atualiza a SRM (mensagem de renovação do sistema) para High-Bandwidth HDCP (Proteção de Conteúdo Digital). |
| [**OPM \_ SET \_ PROTECTION \_ LEVEL**](opm-set-protection-level.md)                                               | Define o nível de proteção para um mecanismo de proteção de saída.                                       |
| [**DEFINIR NÍVEL DE PROTEÇÃO DO OPM \_ DE ACORDO COM O DVD \_ \_ \_ \_ \_ \_ CSS**](opm-set-protection-level-according-to-css-dvd.md) | Define o nível de proteção HDCP para reprodução de DVD, seguindo as regras CSS (Sistema de Contenção de Conteúdo) do DVD. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de programação do OPM](opm-programming-reference.md)
</dt> <dt>

[Gerenciador de Proteção de Saída](output-protection-manager.md)
</dt> </dl>

 

 



