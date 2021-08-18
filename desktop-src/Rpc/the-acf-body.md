---
title: O corpo do ACF
description: O corpo do ACF contém atributos de configuração que se aplicam a tipos e funções definidos no corpo da interface do arquivo IDL.
ms.assetid: 7d6344d3-1117-40b9-be95-a400b81339d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1446b4f0e14849832766bc512a95d0ae0aeb249cebd814314b617ffa1e1125e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924616"
---
# <a name="the-acf-body"></a>O corpo do ACF

O corpo do ACF contém atributos de configuração que se aplicam a tipos e funções definidos no corpo da interface do arquivo IDL. O corpo do ACF pode estar vazio ou pode conter atributos [**ACF,**](/windows/desktop/Midl/include) [**typedef**](/windows/desktop/Midl/typedef), função e parâmetro. Todos esses itens são opcionais. Atributos aplicados a tipos e funções individuais no corpo do ACF substituem atributos no header do ACF.

O ACF especifica o comportamento no computador local e não afeta os dados transmitidos pela rede. Ele é usado para especificar detalhes de um stub a ser gerado. No modo de compatibilidade de DCE ([**/osf**](/windows/desktop/Midl/-osf)), o ACF não afeta a interação entre stubs, mas entre o stub e o código do aplicativo.

Um parâmetro especificado no ACF deve ser um dos parâmetros especificados no arquivo IDL. A ordem de especificação do parâmetro no ACF não é significativa porque a correspondência é por nome, não por posição. A lista de parâmetros no ACF pode estar vazia, mesmo quando a lista de parâmetros na assinatura IDL correspondente não é (mas isso não é recomendado). Declaradores abstratos (parâmetros sem nome) no arquivo IDL faz com que o compilador MIDL reporte erros ao processar o ACF porque o parâmetro não foi encontrado.

A diretiva **ACF include** especifica os arquivos de header a aparecerem no header gerado como parte de uma instrução de inclusão de pré-processador **C \#** padrão. A palavra-chave ACF **include** difere de uma **\# diretiva include.** A palavra-chave ACF include faz com que a linha "**\# include** *filename*" apareça no arquivo de header gerado, enquanto a diretiva de linguagem C "**\# include** *filename*" faz com que o conteúdo desse arquivo seja colocado no ACF. 

A instrução [**typedef**](/windows/desktop/Midl/typedef) do ACF permite aplicar atributos de tipo ACF a tipos definidos anteriormente no arquivo IDL. A sintaxe **typedef do** ACF difere da sintaxe **typedef** C.

Os atributos de função ACF permitem especificar atributos que se aplicam à função como um todo. Para obter mais informações, consulte **\[** [**código**](/windows/desktop/Midl/code) **\]** , **\[** [**otimizar**](/windows/desktop/Midl/optimize) **\]** e não **\[** [**codificar**](/windows/desktop/Midl/nocode) **\]** .

Os atributos de parâmetro ACF permitem especificar atributos que se aplicam a parâmetros individuais da função. Para obter mais informações, consulte **\[** [**contagem de \_ byte**](/windows/desktop/Midl/byte-count) **\]** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**/app \_ config**](/windows/desktop/Midl/-app-config)
</dt> <dt>

[**/osf**](/windows/desktop/Midl/-osf)
</dt> <dt>

[**\[auto \_ handle\]**](../midl/auto-handle.md)
</dt> <dt>

[**\[Código\]**](../midl/code.md)
</dt> <dt>

[**\[alça \_ explícita\]**](../midl/explicit-handle.md)
</dt> <dt>

[O arquivo IDL (Linguagem de Definição de Interface)](the-interface-definition-language-idl-file.md)
</dt> <dt>

[**\[alça \_ implícita\]**](../midl/implicit-handle.md)
</dt> <dt>

[**Incluem**](/windows/desktop/Midl/include)
</dt> <dt>

[Midl](/windows/desktop/Midl/midl-language-reference)
</dt> <dt>

[**\[nocode\]**](../midl/nocode.md)
</dt> <dt>

[**\[Otimizar\]**](../midl/optimize.md)
</dt> <dt>

[**\[representar \_ como\]**](../midl/represent-as.md)
</dt> <dt>

[**Typedef**](/windows/desktop/Midl/typedef)
</dt> </dl>

 

 