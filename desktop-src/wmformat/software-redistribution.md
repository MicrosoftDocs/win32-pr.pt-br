---
title: Redistribuição de software
description: Redistribuição de software
ms.assetid: 443df640-e74c-4903-b801-f4bd42a04659
keywords:
- Windows SDK de formato de mídia, redistribuição de software
- Formato de sistema avançado (ASF), redistribuição de software
- ASF (formato de sistemas avançados), redistribuição de software
- Windows SDK do formato de mídia, redistribuição
- Formato de sistema avançado (ASF), redistribuição
- ASF (formato de sistemas avançados), redistribuição
- redistribuição de software, sobre
- redistribuição, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b933df9319c342d8ed3502fc66757df2e6d8fd6e8d60309023ced6ffa042d5b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807886"
---
# <a name="software-redistribution"></a>Redistribuição de software

a inclusão do software de formato de mídia Windows em uma instalação de aplicativo é conhecida como redistribuição. o SDK do formato de mídia Windows inclui um pacote de instalação que pode ser incluído na configuração do aplicativo. O pacote de instalação é um arquivo executável chamado wmfdist95.exe. quando você instala o SDK do formato de mídia Windows, o pacote de instalação é copiado para a \\ pasta redist do diretório de instalação (c: \\ wmsdk \\ wmfsdk por padrão).

As seções a seguir fornecem procedimentos e outras informações para a configuração de redistribuição de software.



| Seção                                                                            | Descrição                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Para criar uma configuração de redistribuição](to-create-a-redistribution-setup.md)           | Descreve o procedimento para criar uma instalação de aplicativo.                                                                                                                       |
| [Detectando o status da instalação](detecting-setup-status.md)                               | Fornece um código de exemplo que verifica o status de instalação do registro para determinar se o pacote de redistribuição precisa ser instalado.                                    |
| [Exemplo de código para configuração de redistribuição](example-code-for-redistribution-setup.md) | Fornece um código de exemplo que pode ser usado em sua rotina de instalação para executar os pacotes de redistribuição no modo silencioso e notificar sua rotina de instalação quando o computador precisar ser reiniciado. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Project Considere**](project-considerations.md)
</dt> </dl>

 

 




