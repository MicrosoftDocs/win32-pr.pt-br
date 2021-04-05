---
description: Este tópico fornece as práticas recomendadas e sugestões para validar e solucionar problemas de suas implementações IWordBreaker e IStemmer.
ms.assetid: b0e199b9-8d81-4445-92f7-de9b8a00a9cb
title: Solucionando problemas de recursos de idioma e práticas recomendadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63a0a8acda3fff1627b37f41c2d81a67b37d66a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646854"
---
# <a name="troubleshooting-language-resources-and-best-practices"></a>Solucionando problemas de recursos de idioma e práticas recomendadas

Este tópico fornece as práticas recomendadas e sugestões para validar e solucionar problemas de suas implementações [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) e [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) .

Este tópico é organizado da seguinte maneira:

-   [Práticas recomendadas](#best-practices)
-   [Testando a consistência do lematizador](#testing-stemmer-consistency)
-   [Testando a entrada inválida no lematizador](#testing-for-invalid-input-in-the-stemmer)
-   [Testando consistência do separador de palavras](#testing-word-breaker-consistency)
-   [Testando a entrada inválida no separador de palavras](#testing-for-invalid-input-in-the-word-breaker)

### <a name="best-practices"></a>Práticas Recomendadas

-   Verifique se o modelo de threading para recursos de idioma está definido como "ambos" no registro.
-   Sempre que possível, coloque os dados de idioma em um recurso em sua DLL em vez de em um arquivo separado. Isso torna a DLL mais fácil de instalar e mais segura. Além disso, colocar dados de idioma em um recurso resultará em um desempenho aprimorado para esse componente de recurso de linguagem.
-   Minimize os recursos do sistema que os componentes de recursos de idioma usam. Por exemplo, se cada instância de um objeto de recurso de linguagem precisar de acesso somente leitura a um léxico, considere compartilhar o léxico em todas as instâncias.
-   Considere usar o separador de palavras neutro para manipular texto que não está no idioma ou na localidade da implementação do seu separador de palavras. Isso ajudará a garantir que o texto seja processado consistentemente em todos os idiomas.
-   Verifique todos os códigos de retorno e retorne-os de funções como [**IStemmer:: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) e [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext). Se a indexação falhar, é importante passar o erro para que o usuário seja notificado sobre quais documentos foram indexados.

### <a name="testing-stemmer-consistency"></a>Testando a consistência do lematizador

Recomendamos que você monitore o desempenho de uma implementação [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) para fins de consistência sob as seguintes condições:

-   O lematizador executa consistentemente em várias chamadas para [**IStemmer:: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-init). O lematizador reinicializa com os mesmos parâmetros da inicialização anterior, sem liberar os parâmetros.
-   Considerando o mesmo corpus de teste e repetições da mesma consulta, [**IStemmer:: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) produz a saída idêntica e faz chamadas idênticas para os métodos do objeto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) .

### <a name="testing-for-invalid-input-in-the-stemmer"></a>Testando a entrada inválida no lematizador

Recomendamos que você monitore como os métodos [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) lidam com todos os erros relacionados a parâmetros inválidos. Além disso, recomendamos que você garanta que os métodos de lematizador não gerem exceções sem tratamento. O lematizador deve lidar com os seguintes erros:

-   Chamada para [**IStemmer:: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-init) com *PfLicense* definido como **NULL**. Init falha e não resulta em uma violação de acesso.
-   Chamada para [**IStemmer:: GetLicenseToUse**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-getlicensetouse) com o parâmetro *PpwcsLicense* definido como **NULL**. **IStemmer:: GetLicenseToUse** não resulta em violação de acesso.
-   Chamada para [**IStemmer:: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) com o parâmetro *PwcInBuf* definido como **NULL**. **IStemmer:: GenerateWordForms** falha (retorna E \_ falha) e não resulta em uma violação de acesso.
-   Chamada para [**IStemmer:: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) com o parâmetro *CWC* igual a 0. **IStemmer:: GenerateWordForms** retorna com êxito (retorna S \_ OK) e não resulta em uma violação de acesso.
-   Chamada para [**IStemmer:: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) com o parâmetro *PwcInBuf* definido como **NULL** e o parâmetro *CWC* igual a 0. **IStemmer:: GenerateWordForms** falha (retorna E \_ falha) e não resulta em uma violação de acesso.

### <a name="testing-word-breaker-consistency"></a>Testando consistência do separador de palavras

É recomendável que você garanta que a implementação de [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) seja executada consistentemente sob as seguintes condições:

-   O separador de palavras executa consistentemente em várias chamadas para o método [**IWordBreaker:: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-init) . O separador de palavras reinicializa com os mesmos parâmetros da inicialização anterior, sem liberar os parâmetros.
-   Considerando o mesmo corpus de teste e repetições da mesma consulta, o método [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) produz a saída idêntica e faz chamadas idênticas para os métodos dos objetos [**IWordSink**](iwordsink.md) e [**IPhraseSink**](/windows/win32/api/indexsrv/nn-indexsrv-iphrasesink) .

### <a name="testing-for-invalid-input-in-the-word-breaker"></a>Testando a entrada inválida no separador de palavras

Recomendamos que você garanta que os métodos [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) manipulem todos os erros relacionados a parâmetros inválidos. Além disso, recomendamos que você garanta que os métodos de separador de palavras não gerem exceções sem tratamento. O separador de palavras deve executar as seguintes funções e manipular os seguintes erros:

-   A chamada para [**IWordBreaker:: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-init) deve retornar o idioma \_ E o banco de \_ dados \_ não \_ encontrados ou S \_ OK.
-   A chamada para [**IWordBreaker:: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-init) inicializa com êxito o parâmetro *pfLicense* para **false** e chama [**IStemmer:: GetLicenseToUse**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-getlicensetouse) e não resulta em uma violação de acesso.
-   O separador de palavras não é lido após o final do parâmetro *awcBuffer* no método [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) .
-   Chamada para [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) com *PwcInBuf* definido como **NULL**. **IWordBreaker:: BreakText** falha (retorna E \_ falha) e não resulta em uma violação de acesso.
-   Chamada para [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) com o parâmetro *CWC* igual a 0. **IWordBreaker:: BreakText** retorna com êxito (retorna S \_ OK) e não resulta em uma violação de acesso.
-   Chame para o método [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) com o parâmetro *PwcInBuf* definido como **NULL** e o parâmetro *CWC* igual a 0. **IWordBreaker:: BreakText** falha (retorna E \_ falha) e não resulta em uma violação de acesso.
-   As frases geradas durante a criação do índice contêm o mesmo número de palavras.
-   As frases são geradas durante a criação do índice por meio de chamadas sucessivas para os métodos [**IWordFormSink::P utword**](iwordsink-putword.md) e [**IWordFormSink::P utaltword**](iwordsink-putaltword.md) . O separador de palavras usa apenas o objeto [**IPhraseSink**](/windows/win32/api/indexsrv/nn-indexsrv-iphrasesink) durante o tempo de consulta.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estendendo recursos de idioma](extending-language-resources-in-windows-search.md)
</dt> <dt>

[Noções básicas sobre componentes de recursos de idioma](understanding-language-resource-components.md)
</dt> <dt>

[Implementando um separador de palavras e lematizador](implementing-a-word-breaker-and-stemmer.md)
</dt> <dt>

[Considerações lingüísticas e Unicode](linguistic-and-unicode-considerations.md)
</dt> </dl>

 

 
