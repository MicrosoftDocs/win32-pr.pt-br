---
title: Implementando a página de propriedades para um plug-in do DSP
description: Implementando a página de propriedades para um plug-in do DSP
ms.assetid: 3dd3e547-fd06-4f01-8731-da1f8c958a32
keywords:
- plug-ins Windows Media Player, DSP de áudio
- plug-ins, DSP de áudio
- plug-ins de processamento de sinal digital, propriedades de áudio
- Plug-ins do DSP, propriedades de áudio
- plug-ins do DSP de áudio, propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac64dbd1e984d649a4405341d907ddd0c93eabce855bed90e83f698b778a3a2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119617306"
---
# <a name="implementing-the-property-page-for-a-dsp-plug-in"></a>Implementando a página de propriedades para um plug-in do DSP

Windows Media Player pode exibir uma página de propriedades para cada plug-in do DSP para permitir que os usuários definam valores que alteram o comportamento do plug-in. Os usuários podem acessar a página de propriedades da guia **plug-ins** da caixa de diálogo opções clicando no nome do plug-in do DSP para selecioná-lo e, em seguida, clicando em **Propriedades**.

o código de exemplo do assistente de Plug-in de Windows Media Player fornece uma implementação padrão de uma página de propriedades que inclui uma única caixa de edição que recebe do usuário um valor que representa um fator de escala para o volume de áudio. Quando o usuário clica em **aplicar**, a página de propriedades passa esse valor para o objeto de plug-in para que o plug-in possa alterar o valor que ele usa para dimensionar o volume durante o processamento.

## <a name="about-the-property-page-object"></a>Sobre o objeto da página de propriedades

O objeto da página de propriedades é um objeto COM que implementa a interface **IPropertyPage** . O código de exemplo gerado pelo assistente de plug-in usa a implementação de ATL do **IPropertyPage**, que está documentada na documentação do Visual C++ no msdn. Seu código pelo menos deve fornecer implementações de substituição para **IPropertyPage:: OnInitDialog**, que manipula o evento que ocorre quando a página de propriedades é aberta e **IPropertyPage:: apply**, que manipula o evento que ocorre quando o usuário clica em **aplicar**. O assistente de plug-in gera código de exemplo para cada um desses manipuladores de eventos. A implementação de exemplo de **OnInitDialog** recupera um valor do registro para que ele possa exibir a configuração do fator de escala atual. A implementação de exemplo de **Apply** valida a entrada do usuário testando para garantir que ela esteja dentro de um intervalo especificado e, em seguida, persiste o valor no registro e, em seguida, passe o valor (se for válido) para o método Put do plug-in do DSP, chamado **Put de \_ escala**.

Além disso, você precisará adicionar código para manipular o evento que ocorre quando o usuário altera um valor em um controle que você fornece na página de propriedades. Por exemplo, o assistente de plug-in implementa uma função chamada **OnChangeScale**, que simplesmente habilita o botão **Apply** quando o usuário altera o texto na caixa de edição na página de propriedades chamando o método **SetDirty** com um valor de argumento **true**.

## <a name="about-the-property-page-dialog-resource"></a>Sobre o recurso de caixa de diálogo de página de propriedades

A interface do usuário para a página de propriedades é armazenada como um recurso de caixa de diálogo. você pode exibir e editar facilmente a caixa de diálogo de página de propriedades em Visual Studio selecionando a guia **ResourceView** na janela do espaço de trabalho Project, em seguida, abrindo a pasta **caixa de diálogo** e clicando duas vezes no nome do recurso da página de propriedades. o editor de recursos de caixa de diálogo no Visual Studio fornece as ferramentas necessárias para adicionar controles à caixa de diálogo de página de propriedades e criar manipuladores de eventos que são mapeados para as mensagens de Windows apropriadas. para obter detalhes sobre como usar o editor de recursos no Visual Studio, consulte a ajuda do Visual Studio.

## <a name="about-ispecifypropertypages"></a>Sobre o ISpecifyPropertyPages

Se um plug-in do DSP fornecer uma página de propriedades, o plug-in deverá implementar a interface **ISpecifyPropertyPages** . Essa interface contém apenas um método: **ISpecifyPropertyPages:: GetPages**. Esse é o método que associa a página de propriedades ao plug-in do DSP. Windows Media Player chama esse método quando o usuário chama a página de propriedades, passando um parâmetro do tipo CAUUID, que é uma matriz contada de guids. A implementação de plug-in de exemplo de **GetPages** preenche essa estrutura com um único GUID que é a ID de classe do objeto da página de propriedades de plug-in. Windows Media Player, em seguida, usa a id de classe para criar o objeto da página de propriedades.

Você pode observar que a implementação de exemplo de **GetPages** usa **CoTaskMemAlloc** para alocar memória para a estrutura de GUID. é responsabilidade do chamador, neste caso Windows Media Player, para usar o **CoTaskMemFree** para liberar a memória. Para obter detalhes sobre a estrutura CAUUID, consulte a documentação do Platform SDK.

## <a name="about-the-proxystub-dll"></a>Sobre a DLL de proxy/stub

para que um plug-in do DSP funcione no Windows Media Player 11 em execução no Windows Vista, você deve fornecer uma DLL de proxy/stub para interfaces personalizadas usadas para comunicar alterações nas configurações de uma caixa de diálogo de página de propriedades para a classe de plug-in. As chamadas de método feitas por meio dessas interfaces devem ser empacotadas quando as chamadas são feitas entre limites de processo ou de apartamento. A versão mais recente do assistente de plug-in cria um exemplo de projeto de DLL de proxy/stub.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando um plug-in do DSP de áudio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




