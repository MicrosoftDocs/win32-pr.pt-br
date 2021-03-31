---
title: Redistribuição de software
description: Redistribuição de software
ms.assetid: 443df640-e74c-4903-b801-f4bd42a04659
keywords:
- SDK do Windows Media Format, redistribuição de software
- Formato de sistema avançado (ASF), redistribuição de software
- ASF (formato de sistemas avançados), redistribuição de software
- SDK do Windows Media Format, redistribuição
- Formato de sistema avançado (ASF), redistribuição
- ASF (formato de sistemas avançados), redistribuição
- redistribuição de software, sobre
- redistribuição, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d51f332f5b0e038293a1dbe1dbf59015931d67e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635560"
---
# <a name="software-redistribution"></a>Redistribuição de software

A inclusão do software Windows Media Format em uma instalação de aplicativo é conhecida como redistribuição. O SDK do Windows Media Format inclui um pacote de instalação que pode ser incluído na instalação do aplicativo. O pacote de instalação é um arquivo executável chamado wmfdist95.exe. Quando você instala o SDK do Windows Media Format, o pacote de instalação é copiado para a \\ pasta redist do diretório de instalação (c: \\ WMSDK \\ wmfsdk por padrão).

As seções a seguir fornecem procedimentos e outras informações para a configuração de redistribuição de software.



| Seção                                                                            | Descrição                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Para criar uma configuração de redistribuição](to-create-a-redistribution-setup.md)           | Descreve o procedimento para criar uma instalação de aplicativo.                                                                                                                       |
| [Detectando o status da instalação](detecting-setup-status.md)                               | Fornece um código de exemplo que verifica o status de instalação do registro para determinar se o pacote de redistribuição precisa ser instalado.                                    |
| [Exemplo de código para configuração de redistribuição](example-code-for-redistribution-setup.md) | Fornece um código de exemplo que pode ser usado em sua rotina de instalação para executar os pacotes de redistribuição no modo silencioso e notificar sua rotina de instalação quando o computador precisar ser reiniciado. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Considerações sobre o projeto**](project-considerations.md)
</dt> </dl>

 

 




