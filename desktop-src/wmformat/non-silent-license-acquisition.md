---
title: Aquisição de licença não silenciosa
description: Aquisição de licença não silenciosa
ms.assetid: 3b3fce53-9202-4e55-82d5-7c70ea833087
keywords:
- Windows SDK do formato de mídia, aquisição de licença não silenciosa
- Windows SDK do formato de mídia, licenças
- DRM (gerenciamento de direitos digitais), aquisição de licença não silenciosa
- DRM (gerenciamento de direitos digitais), aquisição de licença não silenciosa
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- APIs estendidas do cliente DRM, aquisição de licença não silenciosa
- APIs estendidas do cliente, aquisição de licença não silenciosa
- aquisição de licença não silenciosa
- licenças, aquisição de licença não silenciosa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92c9350e429a1fe4b6218878d2211b355c1569b39284161f9f3abceac1afc6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846422"
---
# <a name="non-silent-license-acquisition"></a>Aquisição de licença não silenciosa

A aquisição de licença não silenciosa permite que o provedor de licenças interaja com o usuário final por meio de uma página da Web, como uma etapa intermediária no processo de aquisição de licença. A aquisição de licença não silenciosa é iniciada em resposta a um usuário que está tentando acessar o conteúdo protegido.

Para executar a aquisição de licença não silenciosa, use as seguintes etapas:

1.  Chame o método [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) . Passe o cabeçalho DRM do arquivo protegido como o parâmetro *bstrHeaderData* . Especifique quais direitos você deseja que a licença conceda no parâmetro *bstrActions* . Por fim, defina o parâmetro *dwFlags* como WMDRM \_ adquirir licença não \_ \_ silenciosa.
2.  Interceptar eventos para a interface **IWMDRMLicenseManagement** . Quando você receber o evento **MEWMDRMLicenseAcquisitionCompleted** , obtenha seu valor associado chamando **IMFMediaEvent:: GetValue**. O valor deve ser do tipo VT \_ desconhecido, um ponteiro para uma interface **IUnknown** .
3.  Chame o método **QueryInterface** da interface **IUnknown** recuperada na etapa 2 para obter a interface [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) .
4.  Chame [**IWMDRMNonSilentLicenseAquisition:: Getdesafiator**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) para recuperar o desafio de licença. Além disso, chame [**IWMDRMNonSilentLicenseAquisition:: getURL**](iwmdrmnonsilentlicenseaquisition-geturl.md) se você ainda não tiver a URL do servidor de licença.
5.  Envie o desafio para a página da Web especificada pela URL.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Adquirindo licenças**](acquiring-licenses.md)
</dt> <dt>

[**Usando o modelo de evento Media Foundation**](using-the-media-foundation-model.md)
</dt> </dl>

 

 




