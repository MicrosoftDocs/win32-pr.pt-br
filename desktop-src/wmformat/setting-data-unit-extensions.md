---
title: Definindo extensões de unidade de dados
description: Definindo extensões de unidade de dados
ms.assetid: 28328c9e-8590-48b8-92b6-1c0475978246
keywords:
- ASF (Advanced Systems Format), extensões de unidade de dados
- ASF (formato de sistemas avançados), extensões de unidade de dados
- extensões de unidade de dados, configurando
- fluxos, extensões de unidade de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822a05a6e6bcbb9f0101d32eed05f2b6c5c68dc8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104499002"
---
# <a name="setting-data-unit-extensions"></a>Definindo extensões de unidade de dados

Alguns fluxos são configurados para usar extensões de unidade de dados para associar dados complementares a exemplos individuais. Para obter mais informações sobre amostras estendidas, consulte [extensões de unidade de dados](data-unit-extensions.md).

A maioria dos sistemas de extensão de unidade de dados requer uma extensão em cada exemplo no fluxo. Se você não fornecer uma extensão do tamanho correto, o gravador rejeitará o exemplo.

Para adicionar dados estendidos a um exemplo, use o método [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) . Você pode obter informações sobre as extensões de unidade de dados configuradas em um fluxo usando os métodos [**IWMStreamConfig2:: GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) e [**IWMStreamConfig2:: GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurar extensões de unidade de dados**](configuring-data-unit-extensions.md)
</dt> <dt>

[**Gravando arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




