---
title: O corpo de ACF
description: O corpo de ACF contém atributos de configuração que se aplicam a tipos e funções definidos no corpo da interface do arquivo IDL.
ms.assetid: 7d6344d3-1117-40b9-be95-a400b81339d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19422762c61dee63c4f502448197aefb432c80c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104008513"
---
# <a name="the-acf-body"></a>O corpo de ACF

O corpo de ACF contém atributos de configuração que se aplicam a tipos e funções definidos no corpo da interface do arquivo IDL. O corpo do ACF pode estar vazio ou pode conter atributos de ACF [**include**](/windows/desktop/Midl/include), [**typedef**](/windows/desktop/Midl/typedef), Function e Parameter. Todos esses itens são opcionais. Atributos aplicados a tipos individuais e funções no corpo de ACF substituem atributos no cabeçalho ACF.

O ACF especifica o comportamento no computador local e não afeta os dados transmitidos pela rede. Ele é usado para especificar detalhes de um stub a ser gerado. No modo de compatibilidade DCE ([**/OSF**](/windows/desktop/Midl/-osf)), o ACF não afeta a interação entre os stubs, mas entre o stub e o código do aplicativo.

Um parâmetro especificado no ACF deve ser um dos parâmetros especificados no arquivo IDL. A ordem de especificação do parâmetro no ACF não é significativa porque a correspondência é por nome, não pela posição. A lista de parâmetros no ACF pode estar vazia, mesmo quando a lista de parâmetros na assinatura IDL correspondente não é (mas não é recomendável). Os declaradores abstratos (parâmetros sem nome) no arquivo IDL fazem com que o compilador MIDL Relate erros durante o processamento do ACF porque o parâmetro não foi encontrado.

A diretiva ACF **include** especifica os arquivos de cabeçalho a serem exibidos no cabeçalho gerado como parte de uma instrução de **\# inclusão** padrão do C-pré-processador. A palavra-chave ACF **inclui** difere de uma diretiva **\# include** . A palavra-chave ACF **include** faz com que a linha "**\# include** *filename*" apareça no arquivo de cabeçalho gerado, enquanto a diretiva C-Language "**\# include** *filename*" faz com que o conteúdo desse arquivo seja colocado no ACF.

A instrução de [**typedef**](/windows/desktop/Midl/typedef) de ACF permite aplicar atributos de tipo de ACF a tipos definidos anteriormente no arquivo IDL. A sintaxe de **typedef** de ACF difere da sintaxe de **typedef** C.

Os atributos da função ACF permitem que você especifique atributos que se aplicam à função como um todo. Para obter mais informações, consulte **\[** [**código**](/windows/desktop/Midl/code) **\]** , **\[** [**otimizar**](/windows/desktop/Midl/optimize) **\]** e **\[** [**Nocode**](/windows/desktop/Midl/nocode) **\]** .

Os atributos de parâmetro de ACF permitem especificar atributos que se aplicam a parâmetros individuais da função. Para obter mais informações, consulte **\[** [**\_ contagem de bytes**](/windows/desktop/Midl/byte-count) **\]** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**configuração do/App \_**](/windows/desktop/Midl/-app-config)
</dt> <dt>

[**/osf**](/windows/desktop/Midl/-osf)
</dt> <dt>

[**\[\_identificador automático\]**](../midl/auto-handle.md)
</dt> <dt>

[**\[auto-completar\]**](../midl/code.md)
</dt> <dt>

[**\[\_identificador explícito\]**](../midl/explicit-handle.md)
</dt> <dt>

[O arquivo IDL (Interface Definition Language)](the-interface-definition-language-idl-file.md)
</dt> <dt>

[**\[\_identificador implícito\]**](../midl/implicit-handle.md)
</dt> <dt>

[**incluir**](/windows/desktop/Midl/include)
</dt> <dt>

[MIDL](/windows/desktop/Midl/midl-language-reference)
</dt> <dt>

[**\[Nocode\]**](../midl/nocode.md)
</dt> <dt>

[**\[formato\]**](../midl/optimize.md)
</dt> <dt>

[**\[representar \_ como\]**](../midl/represent-as.md)
</dt> <dt>

[**typedef**](/windows/desktop/Midl/typedef)
</dt> </dl>

 

 