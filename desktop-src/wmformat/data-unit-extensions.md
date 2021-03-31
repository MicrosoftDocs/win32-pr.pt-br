---
title: Extensões de unidade de dados
description: Extensões de unidade de dados
ms.assetid: f95de189-0449-4b88-aba3-7b19f385c8fe
keywords:
- SDK do Windows Media Format, extensões de unidade de dados
- ASF (Advanced Systems Format), extensões de unidade de dados
- ASF (formato de sistemas avançados), extensões de unidade de dados
- SDK do Windows Media Format, sistemas de extensão de carga
- ASF (Advanced Systems Format), sistemas de extensão de carga
- ASF (formato de sistemas avançados), sistemas de extensão de carga
- extensões de unidade de dados, sobre
- extensões de unidade de carga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8ed5c9db82d0002648148ca14bd7f94baa9029
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640145"
---
# <a name="data-unit-extensions"></a>Extensões de unidade de dados

O SDK do Windows Media Format permite que você complemente dados em exemplos com *extensões de unidade de dados*, também chamadas de sistemas de extensão de carga. Esta documentação usa o termo "extensões de unidade de dados" para permanecer consistente com nomes de métodos como [**AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension). Uma extensão de unidade de dados é um par de nome/valor que é anexado ao exemplo na seção de dados do arquivo. Você pode acessar os dados estendidos usando métodos do objeto buffer quando o exemplo é recuperado pelo leitor.

Você pode criar extensões de unidade de dados para suas próprias especificações, mas vários tipos são predefinidos e suportados pelos objetos desse SDK. Essas extensões padrão são usadas para fornecer dados adicionais para nomes de arquivo (em fluxos de script e Web), dados de código de tempo SMPTE, taxa de proporção de pixel não quadrado, duração e tipo de entrelaçamento.

Para usar extensões de unidade de dados, você deve configurar o fluxo para aceitá-los e, em seguida, adicionar extensões a cada exemplo para esse fluxo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de arquivo ASF**](asf-file-features.md)
</dt> <dt>

[**Configurar extensões de unidade de dados**](configuring-data-unit-extensions.md)
</dt> <dt>

[**Definindo extensões de unidade de dados**](setting-data-unit-extensions.md)
</dt> </dl>

 

 




