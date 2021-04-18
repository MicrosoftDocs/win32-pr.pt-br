---
description: Você faz referência a um reconhecedor de tinta com um identificador HRECOGNIZER e um contexto de reconhecedor como um identificador HRECOCONTEXT. Uma DLL (biblioteca de vínculo dinâmico) do reconhecedor pode implementar reconhecedores para mais de um idioma.
ms.assetid: 23002d02-cf8f-489b-a50f-4a18ac091825
title: HRECOGNIZER e HRECOCONTEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12af1bb5569a22a612f0a3ed667a55aac81da2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787698"
---
# <a name="hrecognizer-and-hrecocontext"></a>HRECOGNIZER e HRECOCONTEXT

Você faz referência a um reconhecedor de tinta com um identificador [HRECOGNIZER](hrecognizer-handle.md) e um contexto de reconhecedor como um identificador [HRECOCONTEXT](hrecocontext-handle.md) .

Uma DLL (biblioteca de vínculo dinâmico) do reconhecedor pode implementar reconhecedores para mais de um idioma. Nesse caso, cada idioma é selecionado por um CLSID que é passado ao criar o objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) no aplicativo. Além disso, uma DLL de reconhecimento pode criar vários identificadores de reconhecedor quando ele é carregado, um ou mais para cada idioma reconhecido.

Um contexto de reconhecedor é criado para representar o evento de reconhecimento de uma folha de tinta específica. Quando o contexto é criado, o identificador de objetos do reconhecedor associado é passado para a função [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext) . Isso associa o idioma ao contexto do reconhecedor.

Um contexto de reconhecedor pode representar o reconhecimento de toda a tinta no corpo de um email, a tinta de um único campo dentro de um aplicativo ou uma única linha de texto gravada no painel de entrada do Tablet PC. O volume de tinta em um único contexto de reconhecedor pode variar de um único traço para uma página inteira ou mais.

O contexto do reconhecedor é definido pelas configurações de:

-   O guia de reconhecimento.
-   Quaisquer factos.
-   Quaisquer sinalizadores.
-   O contexto do texto.
-   Qualquer lista de palavras.
-   O modo de preenchimento automático de caractere.

O identificador do contexto do reconhecedor é passado para todas as funções que usam essas configurações. Alterar uma configuração altera o contexto do reconhecedor.

O aplicativo pode usar vários contextos para reconhecer tinta de diferentes partes da tela. Um contexto individual pode reconhecer várias linhas de texto. No entanto, um contexto individual não pode processar dois parágrafos gravados lado a lado, como várias colunas em um artigo de jornal.

Para reconhecer a nova tinta, crie um novo contexto. Como alternativa, use a função [**CloneContext**](/windows/desktop/api/recapis/nf-recapis-clonecontext) para fazer uma cópia de um contexto que não tem a tinta e os resultados, ou a função [**ResetContext**](/windows/desktop/api/recapis/nf-recapis-resetcontext) para limpar um contexto de sua tinta e dos resultados. Com essas abordagens, um aplicativo de tinta pode reutilizar um contexto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Função setguide**](/windows/desktop/api/recapis/nf-recapis-setguide)
</dt> <dt>

[**Função getguide**](/windows/desktop/api/recapis/nf-recapis-getguide)
</dt> <dt>

[**Função setfactoid**](/windows/desktop/api/recapis/nf-recapis-setfactoid)
</dt> <dt>

[**Função SetFlags**](/windows/desktop/api/recapis/nf-recapis-setflags)
</dt> <dt>

[**Função SetEnabledUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges)
</dt> <dt>

[**Função GetEnabledUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges)
</dt> <dt>

[**Função SetCACMode**](/windows/desktop/api/recapis/nf-recapis-setcacmode)
</dt> <dt>

[**Função SetTextContext**](/windows/desktop/api/recapis/nf-recapis-settextcontext)
</dt> <dt>

[**Função setwordlist**](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 



