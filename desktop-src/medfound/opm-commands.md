---
description: Comandos OPM
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: Comandos OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b00240925c28322b911ab55a0e4f026f051d6ec
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119141"
---
# <a name="opm-commands"></a>Comandos OPM

Esta seção lista os comandos disponíveis para o [Gerenciador de proteção de saída](output-protection-manager.md) (OPM).

Para enviar um comando OPM, chame [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure). Para cada comando, as informações a seguir são listadas.



| Valor             | Descrição                                                                                                                                                            |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de comando | Identifica o comando. Defina o membro **guidSetting** da estrutura de [**configuração de \_ \_ parâmetros de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) igual a esse valor. |
| Dados de entrada   | Especifica como interpretar a matriz **abParameters** na estrutura de [**\_ \_ parâmetros de configuração de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) .                      |



 

Os comandos a seguir são definidos:



| Comando                                                                                                       | Descrição                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**OPM \_ define \_ a \_ \_ sinalização ACP e CGMSA \_**](opm-set-acp-and-cgmsa-signaling.md)                               | Especifica informações sobre o sinal de vídeo, além do nível de proteção.                      |
| [**OPM \_ definido \_ SRM de HDCP \_**](opm-set-hdcp-srm.md)                                                               | Atualiza a mensagem de renovação do sistema (SRM) para o High-Bandwidth digital Proteção de Conteúdo (HDCP). |
| [**OPM \_ definir \_ nível de proteção \_**](opm-set-protection-level.md)                                               | Define o nível de proteção para um mecanismo de proteção de saída.                                       |
| [**OPM \_ define \_ o \_ nível \_ \_ de proteção de acordo \_ \_ com o DVD do CSS**](opm-set-protection-level-according-to-css-dvd.md) | Define o nível de proteção de HDCP para reprodução de DVD, seguindo as regras de sistema de embaralhamento de conteúdo de DVD (CSS). |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de programação de OPM](opm-programming-reference.md)
</dt> <dt>

[Gerenciador de proteção de saída](output-protection-manager.md)
</dt> </dl>

 

 



