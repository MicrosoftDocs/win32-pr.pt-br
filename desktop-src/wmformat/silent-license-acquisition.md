---
title: Aquisição de licença silenciosa
description: Aquisição de licença silenciosa
ms.assetid: bf88f1bb-0cbb-4c30-92e0-3d342977d67f
keywords:
- Windows SDK de Formato de Mídia, aquisição de licença silenciosa
- Windows SDK de Formato de Mídia, licenças
- DRM (gerenciamento de direitos digitais), aquisição de licença silenciosa
- DRM (gerenciamento de direitos digitais), aquisição silenciosa de licença
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- APIs estendidas do cliente DRM, aquisição silenciosa de licença
- APIs estendidas do cliente, aquisição silenciosa de licença
- aquisição de licença silenciosa
- licenças, aquisição de licença silenciosa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eff454ce673230f0c7dbe6f64afbf46e9bbe8b5f948609f5fb67d647a4151ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197458"
---
# <a name="silent-license-acquisition"></a>Aquisição de licença silenciosa

A aquisição silenciosa de licença requer apenas uma única chamada de método que trata todas as comunicações de rede com o servidor de licença de forma assíncrona.

Esse tipo de aquisição de licença geralmente é usado como uma resposta ao usuário final que está tentando acessar o conteúdo protegido, por exemplo, tentando reproduzir um arquivo protegido em um aplicativo de player de mídia. Como a aquisição de licença silenciosa obtém a licença com uma única chamada, ela não poderá ser usada se a entrada adicional do usuário, como o pagamento pelo conteúdo, for necessária.

Para executar a aquisição silenciosa de licença, use as seguintes etapas:

1.  Chame o [**método IWMDRMLicenseManagement::AcquireLicense.**](iwmdrmlicensemanagement-acquirelicense.md) Passe o header drm do arquivo protegido como o *parâmetro bstrHeaderData.* Especifique quais direitos você deseja que a licença conceda no *parâmetro bstrActions.* Por fim, defina *o parâmetro dwFlags* como WMDRM \_ ACQUIRE LICENSE \_ \_ SILENT.
2.  Intercepte eventos para a interface [**IWMDRMLicenseManagement.**](iwmdrmlicensemanagement.md) Quando você receber o **evento MEWMDRMLicenseAcquisitionCompleted,** verifique seu código de retorno chamando o método **IMFMediaEvent::GetStatus,** que está documentado na documentação do Media Foundation. Se o valor **HRESULT** recuperado for um código de êxito, a licença foi baixada com êxito e está no armazenamento de licenças local pronta para uso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Adquirir licenças**](acquiring-licenses.md)
</dt> <dt>

[**Usando o modelo Media Foundation evento**](using-the-media-foundation-model.md)
</dt> </dl>

 

 




