---
title: Considerações para mercados internacionais
description: Considerações para mercados internacionais
ms.assetid: 890a280d-a4e0-4349-960d-ca8ac1872ee6
keywords:
- Lojas online do Windows Media Player, mercados internacionais
- lojas online, mercados internacionais
- Digite 1 lojas online, mercados internacionais
- Digite 2 lojas online, mercados internacionais
- mercados internacionais
- Repositórios online do Windows Media Player, documento do serviceInfo
- repositórios online, documento do serviceInfo
- Digite 1 lojas online, documento do serviceInfo
- tipo 2 lojas online, documento do serviceInfo
- Documento do serviceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1822e4f647c9967d50d40fa19331cd58565cf2eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761115"
---
# <a name="considerations-for-international-markets"></a>Considerações para mercados internacionais

Se sua empresa cria lojas online para vários mercados, você deve fornecer à Microsoft a URL de um documento do serviceInfo para cada mercado. Você pode fazer isso de uma das duas maneiras a seguir:

-   Crie um documento do serviceInfo separado para cada mercado. Nesse caso, você fornece à Microsoft URLs que apontam para documentos de informações individuais para cada loja online em cada mercado.
-   Crie um único documento de informações para todos os mercados. Ao fazer isso, você fornece à Microsoft a mesma URL para cada mercado. Seu documento do serviceInfo, criado como uma página ASP, pode, então, detectar dinamicamente a localização do usuário com base em parâmetros de cadeia de caracteres de consulta.

O Windows Media Player acrescenta uma cadeia de caracteres de consulta à solicitação de URL do serviceInfo que fornece informações sobre as configurações de localidade e local do usuário. Se sua loja online usa essas informações para determinar qual conteúdo exibir, você deve acrescentar esses valores dinamicamente às suas próprias URLs no documento do serviceInfo. Essa é a melhor maneira de garantir que as URLs da página da Web sempre conterão os parâmetros esperados.

Depois de determinar a localidade e a preferência de idioma do usuário, talvez você queira manter essas informações para futuras sessões. Você pode fazer isso usando qualquer uma das técnicas que normalmente usaria em uma página da Web, como cookies, ou usando seu objeto COM.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando o documento do serviceInfo dinamicamente**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Informações comuns às lojas online tipo 1 e tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento serviceInfo**](serviceinfo-element.md)
</dt> </dl>

 

 




