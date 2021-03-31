---
title: Chaves de teste e de produção para uma loja online tipo 2
description: Chaves de teste e de produção para uma loja online tipo 2
ms.assetid: 4fce47e2-d73d-4484-9bda-48257268ed96
keywords:
- Armazenamentos online do Windows Media Player, chaves de teste
- lojas online, chaves de teste
- tipo 2 lojas online, chaves de teste
- Lojas online do Windows Media Player, chaves de produção
- lojas online, chaves de produção
- tipo 2 lojas online, chaves de produção
- Repositórios online do Windows Media Player, documento do serviceInfo
- repositórios online, documento do serviceInfo
- tipo 2 lojas online, documento do serviceInfo
- chaves de teste
- chaves de produção
- Documento do serviceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f009e1b0ca58a66820e193e3b66f8ca50ccadc43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916545"
---
# <a name="test-and-production-keys-for-a-type-2-online-store"></a>Chaves de teste e de produção para uma loja online tipo 2

Quando você começa o desenvolvimento de sua loja online, a Microsoft fornece duas chaves numéricas: uma chave de teste e uma chave de produção. Ao mesmo tempo, você deve fornecer à Microsoft duas URLs: uma que aponte para o documento de informações de teste e outra que aponte para seu documento de informações de produção.

Durante o estágio de desenvolvimento e teste, sua loja online ficará visível no Windows Media Player somente se sua chave de teste ou sua chave de produção estiver no registro no computador do usuário. Se a chave de teste estiver no registro, o Windows Media Player recuperará seu documento de informações de teste, que aponta para o plug-in, as páginas da Web e as imagens que pertencem ao seu repositório de teste. Se a chave de produção estiver no registro, o Windows Media Player recuperará o documento de informações de produção, que aponta para o plug-in, as páginas da Web e as imagens que pertencem à sua loja de produção.

Você pode usar seus armazenamentos de teste e produção de qualquer maneira que achar útil. Normalmente, no entanto, a distinção é a seguinte:

-   Seu repositório de teste é o local onde você faz alterações diárias em seu plug-in, páginas da Web, imagens e outros componentes do seu serviço.
-   Sua loja de produção é o local onde você mantém uma liberação estável do seu serviço, que inclui seu plug-in, páginas da Web, imagens e outros componentes.

Antes que sua loja online possa ser publicada no Windows Media Player, a Microsoft deve validar que o serviço é executado corretamente. Durante a fase de validação, a Microsoft usa sua chave de produção. A Microsoft não usa sua chave de teste durante a fase de validação.

Quando seu armazenamento online de produção conclui com êxito o processo de validação, a Microsoft publica sua loja, o que significa que sua loja de produção aparece no Windows Media Player para todos os usuários, não apenas aqueles que têm sua chave de produção no registro. Depois que o armazenamento é publicado, as chaves de teste e de produção não são mais necessárias.

> [!Note]  
> Os usuários podem adivinhar a chave de teste ou de produção para sua loja online e exibir sua loja enquanto ela está sendo desenvolvida. Você deve ter cuidado ao expor os recursos que deseja manter secretos até a liberação pública.

 

Para obter informações detalhadas sobre onde colocar suas chaves de produção e teste no registro do usuário, consulte [chaves e entradas do registro para uma loja online tipo 2](registry-keys-and-entries-for-a-type-2-online-store.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre as lojas online do tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Tipo 2 amostras de loja online**](type-2-online-store-samples.md)
</dt> </dl>

 

 




