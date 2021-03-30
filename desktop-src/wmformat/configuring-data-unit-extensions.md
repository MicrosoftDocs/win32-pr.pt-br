---
title: Configurar extensões de unidade de dados
description: Configurar extensões de unidade de dados
ms.assetid: 5dc0a596-68ae-409a-9abc-15ca507d6ec7
keywords:
- fluxos, configurando extensões de unidade de dados
- fluxos, extensões de unidade de dados
- extensões de unidade de dados, configurando
- perfis, extensões de unidade de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7e6794b95128d180bc3922f9bf03a15a2749df
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "103640285"
---
# <a name="configuring-data-unit-extensions"></a>Configurar extensões de unidade de dados

Exemplos gravados em arquivos ASF podem conter informações adicionais além das amostras de mídia em si. Essas informações são incluídas usando as extensões de unidade de dados. Para obter mais informações sobre extensões de unidade de dados, consulte [extensões de unidade de dados](data-unit-extensions.md).

Para usar extensões de unidade de dados, você deve configurar o fluxo no perfil para aceitá-los. Para configurar uma extensão de unidade de dados para um fluxo, execute as etapas a seguir.

1.  Obtenha um ponteiro para a interface [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) chamando o método **QueryInterface** de [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).
2.  Chame [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) para registrar um tipo de extensão de unidade de dados para o fluxo.

Você pode examinar todos os tipos de extensão de unidade de dados registrados atualmente para um fluxo chamando [**IWMStreamConfig2:: GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) para recuperar o número de tipos de extensão de unidade de dados registrados. Em seguida, você pode executar um loop por todos os tipos usando chamadas para [**IWMStreamConfig2:: GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) para cada.

As extensões de unidade de dados recebem um tamanho quando configuradas para um fluxo. Muitos sistemas de extensão de unidade de dados usam dados que são um tamanho constante (geralmente uma estrutura). No entanto, você também pode configurar suas extensões de unidade de dados para que sejam do tamanho da variável, definindo o tamanho como 0xFFFF. Cada extensão de unidade de dados atribuída no momento da codificação pode ser de qualquer tamanho entre 1 byte e 65534 bytes. As extensões de unidade de dados de tamanho variados também são chamadas de extensões de unidade de dados dinâmicas

A vantagem de usar extensões de unidade de dados dinâmicas é que você pode anexar dados de extensão conforme necessário. Se você definir uma extensão de unidade de dados com um tamanho definido, cada amostra do fluxo deverá conter dados de extensão desse tamanho, mesmo que você não tenha dados para alguns exemplos. Com extensões de unidade de dados dinâmicas, você pode omitir as extensões de unidade de dados de alguns exemplos, o que economiza espaço e reduz os requisitos de largura de banda. No entanto, se as extensões de unidade de dados forem de tamanho variável, o objeto de leitura não poderá verificar os dados de extensão recebidos em relação a um tamanho estático. Você deve verificar se os dados de extensão recebidos são válidos e não há distorção mal-intencionada do fluxo de bits.

As extensões de unidade de dados individuais devem ser definidas em exemplos usando o método [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) . Para obter mais informações, consulte [definindo extensões de unidade de dados](setting-data-unit-extensions.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurando fluxos**](configuring-streams.md)
</dt> </dl>

 

 




