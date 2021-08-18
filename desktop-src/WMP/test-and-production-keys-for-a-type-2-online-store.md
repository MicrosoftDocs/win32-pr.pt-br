---
title: Chaves de teste e produção para uma loja online do tipo 2
description: Chaves de teste e produção para uma loja online do tipo 2
ms.assetid: 4fce47e2-d73d-4484-9bda-48257268ed96
keywords:
- Windows Media Player online, chaves de teste
- lojas online, chaves de teste
- tipo 2 lojas online, chaves de teste
- Windows Media Player online, chaves de produção
- lojas online, chaves de produção
- tipo 2 lojas online, chaves de produção
- Windows Media Player online, documento ServiceInfo
- lojas online, documento ServiceInfo
- type 2 online stores,ServiceInfo document
- chaves de teste
- chaves de produção
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0914417aa58d16c89c31ef0efbba6b5b2df70b69c0df62f809880ced33ee91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118418"
---
# <a name="test-and-production-keys-for-a-type-2-online-store"></a>Chaves de teste e produção para uma loja online do tipo 2

Quando você começa o desenvolvimento de sua loja online, a Microsoft fornece duas chaves numéricas: uma chave de teste e uma chave de produção. Ao mesmo tempo, você deve fornecer à Microsoft duas URLs: uma que aponta para o documento ServiceInfo de teste e outra que aponta para o documento ServiceInfo de produção.

Durante o estágio de desenvolvimento e teste, sua loja online fica visível Windows Media Player somente se a chave de teste ou a chave de produção estiver no Registro no computador do usuário. Se a chave de teste estiver no Registro, o Windows Media Player recuperará o documento ServiceInfo de teste, que aponta para o plug-in, páginas da Web e imagens que pertencem ao seu armazenamento de teste. Se sua chave de produção estiver no Registro, Windows Media Player recuperará o documento ServiceInfo de produção, que aponta para o plug-in, páginas da Web e imagens que pertencem ao seu armazenamento de produção.

Você pode usar suas lojas de teste e produção de qualquer maneira que achar útil. Normalmente, no entanto, a distinção é a seguinte:

-   Seu armazenamento de teste é o local em que você faz alterações diárias em seu plug-in, páginas da Web, imagens e outros componentes do serviço.
-   Seu armazenamento de produção é o local em que você mantém uma versão estável do seu serviço, que inclui seu plug-in, páginas da Web, imagens e outros componentes.

Antes que sua loja online possa ser publicada no Windows Media Player, a Microsoft deve validar se o serviço tem o desempenho correto. Durante a fase de validação, a Microsoft usa sua chave de produção. A Microsoft não usa sua chave de teste durante a fase de validação.

Quando sua loja online de produção conclui com êxito o processo de validação, a Microsoft publica sua loja, o que significa que sua loja de produção aparece no Windows Media Player para todos os usuários, não apenas aqueles que têm sua chave de produção no Registro. Depois que sua loja for publicada, as chaves de teste e produção não serão mais necessárias.

> [!Note]  
> Os usuários podem adivinhar a chave de teste ou produção para sua loja online e exibir sua loja enquanto ela está sendo desenvolvida. Você deve ter cuidado ao expor recursos que deseja manter em segredo até o lançamento público.

 

Para obter informações detalhadas sobre onde colocar suas chaves de produção e teste no Registro do usuário, consulte Chaves e entradas do Registro para uma Loja [Online do Tipo 2.](registry-keys-and-entries-for-a-type-2-online-store.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre as Lojas Online do Tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Exemplos da Loja Online do Tipo 2**](type-2-online-store-samples.md)
</dt> </dl>

 

 




