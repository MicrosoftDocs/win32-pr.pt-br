---
title: Revogação e renovação de componentes automatizados
description: Revogação e renovação de componentes automatizados
ms.assetid: be4899d7-1d87-4450-8c0e-75cf112ca66a
keywords:
- SDK do Windows Media Format, revogação e renovação automatizadas
- SDK do Windows Media Format, revogação
- SDK do Windows Media Format, renovação
- DRM (gerenciamento de direitos digitais), revogação automatizada e renovação
- DRM (gerenciamento de direitos digitais), revogação e renovação automatizadas
- DRM (gerenciamento de direitos digitais), revogação
- DRM (gerenciamento de direitos digitais), revogação
- DRM (gerenciamento de direitos digitais), renovação
- DRM (gerenciamento de direitos digitais), renovação
- APIs estendidas do cliente DRM, revogação e renovação automatizadas
- APIs estendidas do cliente, revogação e renovação automatizadas
- APIs estendidas do cliente DRM, revogação
- APIs estendidas do cliente, revogação
- APIs estendidas do cliente DRM, renovação
- APIs estendidas do cliente, renovação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9046d04d8ca7a138a06cba4d26cd82bc5a12b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294348"
---
# <a name="automated-component-revocation-and-renewal"></a>Revogação e renovação de componentes automatizados

Os aplicativos ou componentes de software considerados comprometidos podem ser revogados pela Microsoft. A API estendida do cliente do Windows Media Format fornece um mecanismo para a revogação automatizada e a renovação de componentes.

Os componentes revogados são listados em uma lista de certificados revogados, que é publicada pela Microsoft. Quando um componente é revogado, seu certificado é adicionado à lista de certificados revogados e o BLOB de informações de revogação ( \_ info Rev) é atualizado nos servidores da Microsoft.

Para executar a revogação automatizada e a renovação quando um usuário tenta processar o conteúdo protegido por DRM do Windows Media, seu aplicativo deve fazer o seguinte:

1.  Extraia a \_ versão de informações de Rev da licença. O número de versão de informações de REV \_ está localizado no seguinte local em uma licença do XMR:
    ```C++
    <LICENSE version="2.0.0.0">
        <LICENSORINFO/>
        <DATA>
            <LID>...</LID>
            <KID>...</KID>
            <RevInfoVersion>42</RevInfoVersion>
            ...
         </DATA>
    ....
    </LICENSE>
    ```

    

2.  Compare o \_ número de versão de informações Rev da licença com o \_ número de versão da info Rev no repositório local chamando o método [**IWMDRMSecurity:: GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md) .
3.  Se a \_ versão de informações Rev não estiver atualizada, chame o método [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) , passando o \_ sinalizador segurança WMDRM \_ executar \_ atualização de revogação \_ no parâmetro *dwFlags* .
4.  Recupere a lista de certificados revogados do armazenamento local chamando o método [**IWMDRMSecurity:: GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) .
5.  Analise a lista de revogação e verifique as revogações do Windows Media DRM. Para obter mais informações, consulte [verificando revogação de certificado](checking-certificate-revocation.md).
6.  Se houver qualquer revogação do Windows Media DRM:
    1.  Crie um habilitador de conteúdo para renovar os componentes revogados chamando o método [**IWMDRMSecurity:: GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) .
    2.  Chame **IMFContentEnabler:: AutomaticEnable** que direciona o usuário para uma URL que contém informações de renovação de componentes. Esse método está documentado no [SDK do Media Foundation](../medfound/microsoft-media-foundation-sdk.md) ( https://msdn.microsoft.com/library/ms694197(VS.85).aspx) .
        > [!Note]  
        > Você deve esclarecer esse processo para o usuário por meio do uso de uma declaração de privacidade, pois o processo de atualização envia informações do computador cliente para um site da Microsoft.

         

    3.  Se possível, o usuário renovará o componente da URL, seja automaticamente ou seguindo instruções específicas. Haverá algumas situações em que o componente não pode ser renovado.
    4.  Tente acessar o conteúdo novamente até que não haja mais revogações ou o processo seja interrompido por algum motivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação**](drm-programming-guide.md)
</dt> </dl>

 

 