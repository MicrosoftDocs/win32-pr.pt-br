---
title: Extensões de unidade de dados
description: Extensões de unidade de dados
ms.assetid: f95de189-0449-4b88-aba3-7b19f385c8fe
keywords:
- Windows SDK de Formato de Mídia, extensões de unidade de dados
- ASF (Advanced Systems Format), extensões de unidade de dados
- ASF (Formato de Sistemas Avançados), extensões de unidade de dados
- Windows SDK de Formato de Mídia, sistemas de extensão de payload
- ASF (Advanced Systems Format), sistemas de extensão de carga
- ASF (Formato de Sistemas Avançados), sistemas de extensão de carga
- extensões de unidade de dados, sobre
- extensões de unidade de carga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 127c173e5056ee14dac3d2100f093d6b3cb1d356113b42f9faa96ef6287217fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118029938"
---
# <a name="data-unit-extensions"></a>Extensões de unidade de dados

O Windows SDK de Formato de Mídia permite complementar dados em exemplos com extensões de unidade de *dados*, também chamados de sistemas de extensão de carga. Esta documentação usa o termo "extensões de unidade de dados" para permanecer consistente com nomes de método, como [**AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension). Uma extensão de unidade de dados é um par nome/valor anexado ao exemplo na seção de dados do arquivo. Você pode acessar os dados estendidos usando métodos do objeto de buffer quando o exemplo é recuperado pelo leitor.

Você pode criar extensões de unidade de dados para suas próprias especificações, mas vários tipos são predefinidos e com suporte pelos objetos desse SDK. Essas extensões padrão são usadas para fornecer dados adicionais para nomes de arquivo (em scripts e fluxos web), dados de código de tempo SMPTE, taxa de proporção de pixel não quadrado, duração e tipo de entrelaçamento.

Para usar extensões de unidade de dados, você deve configurar o fluxo para aceitá-las e, em seguida, adicionar extensões a cada exemplo desse fluxo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de arquivo ASF**](asf-file-features.md)
</dt> <dt>

[**Configurar extensões de unidade de dados**](configuring-data-unit-extensions.md)
</dt> <dt>

[**Configurando extensões de unidade de dados**](setting-data-unit-extensions.md)
</dt> </dl>

 

 




