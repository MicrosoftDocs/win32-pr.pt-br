---
title: Configurando extensões de unidade de dados
description: Configurando extensões de unidade de dados
ms.assetid: 28328c9e-8590-48b8-92b6-1c0475978246
keywords:
- ASF (Advanced Systems Format), extensões de unidade de dados
- ASF (Formato de Sistemas Avançados), extensões de unidade de dados
- extensões de unidade de dados, configuração
- fluxos, extensões de unidade de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1bb88e9aa0c3bc00d4c21a1c262b7ff4a44fbc2f426f139b3b782a0bbdb7b83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197478"
---
# <a name="setting-data-unit-extensions"></a>Configurando extensões de unidade de dados

Alguns fluxos são configurados para usar extensões de unidade de dados para associar dados suplementares a exemplos individuais. Para obter mais informações sobre exemplos estendidos, consulte [Extensões de unidade de dados](data-unit-extensions.md).

A maioria dos sistemas de extensão de unidade de dados exige uma extensão em cada exemplo no fluxo. Se você não fornecer uma extensão do tamanho correto, o autor rejeitará o exemplo.

Para adicionar dados estendidos a um exemplo, use o [**método INSSBuffer3::SetProperty.**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) Você pode obter informações sobre as extensões de unidade de dados configuradas em um fluxo usando os métodos [**IWMStreamConfig2::GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) e [**IWMStreamConfig2::GetDataUnitExtension.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurar extensões de unidade de dados**](configuring-data-unit-extensions.md)
</dt> <dt>

[**Escrevendo arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




