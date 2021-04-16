---
title: Aquisição de licença não silenciosa
description: Aquisição de licença não silenciosa
ms.assetid: 3b3fce53-9202-4e55-82d5-7c70ea833087
keywords:
- SDK do Windows Media Format, aquisição de licença não silenciosa
- SDK do Windows Media Format, licenças
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
ms.openlocfilehash: adb8d7c4865e74fd5ce383cff8317de905828afe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498800"
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

 

 




