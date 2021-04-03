---
title: Aquisição de licença silenciosa
description: Aquisição de licença silenciosa
ms.assetid: bf88f1bb-0cbb-4c30-92e0-3d342977d67f
keywords:
- SDK do Windows Media Format, aquisição de licença silenciosa
- SDK do Windows Media Format, licenças
- DRM (gerenciamento de direitos digitais), aquisição de licença silenciosa
- DRM (gerenciamento de direitos digitais), aquisição de licença silenciosa
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- APIs estendidas do cliente DRM, aquisição de licença silenciosa
- APIs estendidas do cliente, aquisição de licença silenciosa
- aquisição de licença silenciosa
- licenças, aquisição de licença silenciosa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ef92eaf4e347e8eb30f56c1111ec5b27f1e62d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005806"
---
# <a name="silent-license-acquisition"></a>Aquisição de licença silenciosa

A aquisição de licença silenciosa requer apenas uma chamada de método única que manipule todas as comunicações de rede com o servidor de licença de forma assíncrona.

Esse tipo de aquisição de licença geralmente é usado como uma resposta ao usuário final que está tentando acessar o conteúdo protegido — por exemplo, tentar reproduzir um arquivo protegido em um aplicativo de player de mídia. Como a aquisição de licença silenciosa Obtém a licença com uma única chamada, ela não pode ser usada se forem necessárias entradas adicionais do usuário, como o pagamento do conteúdo.

Para executar a aquisição de licença silenciosa, use as seguintes etapas:

1.  Chame o método [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) . Passe o cabeçalho DRM do arquivo protegido como o parâmetro *bstrHeaderData* . Especifique quais direitos você deseja que a licença conceda no parâmetro *bstrActions* . Por fim, defina o parâmetro *dwFlags* como WMDRM \_ adquirir \_ licença \_ silenciosa.
2.  Interceptar eventos para a interface [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) . Ao receber o evento **MEWMDRMLicenseAcquisitionCompleted** , verifique seu código de retorno chamando o método **IMFMediaEvent:: GetStatus** , que está documentado na documentação do Media Foundation. Se o valor **HRESULT** recuperado for um código de êxito, a licença foi baixada com êxito e estará no repositório de licenças local pronto para uso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Adquirindo licenças**](acquiring-licenses.md)
</dt> <dt>

[**Usando o modelo de evento Media Foundation**](using-the-media-foundation-model.md)
</dt> </dl>

 

 




