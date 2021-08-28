---
title: Exportando conteúdo compactado
description: Exportando conteúdo compactado
ms.assetid: b312aa5e-d693-4d0a-9d74-b443713cec8c
keywords:
- Windows SDK de formato de mídia, exportação de DRM
- Windows Media Format SDK, exportar
- Windows SDK do formato de mídia, conteúdo compactado
- DRM (gerenciamento de direitos digitais), exportar
- DRM (gerenciamento de direitos digitais), exportar
- DRM (gerenciamento de direitos digitais), conteúdo compactado
- DRM (gerenciamento de direitos digitais), conteúdo compactado
- APIs estendidas do cliente DRM, conteúdo compactado
- APIs estendidas do cliente, conteúdo compactado
- APIs estendidas do cliente DRM, exportar
- APIs estendidas do cliente, exportar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e7e8e6d71e4104d65336b131d0e15d5eaedd8b2fba4b7715f5e60aa6083544
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055496"
---
# <a name="exporting-compressed-content"></a>Exportando conteúdo compactado

esta seção descreve como exportar Windows mídia protegida por DRM de mídia em um arquivo de mídia Windows em que o aplicativo recebe dados de mídia digital compactados. para fazer isso, seu aplicativo deve executar a descriptografia embutida de todos os Windows cargas criptografadas de DRM de mídia em um arquivo ASF.

> [!Note]  
> uma biblioteca de análise de ASF é fornecida a você como parte do contrato de exportação de DRM de mídia Windows.

 

As principais etapas envolvidas na exportação de conteúdo compactado são:

1.  Execute a individualização de DRM, se necessário.
2.  Verifique se o esquema de proteção de conteúdo de destino é explicitamente permitido.
3.  Crie um objeto de descriptografia para descriptografar cada carga de ASF.
4.  o sistema DRM criptografa cada carga ASF de Windows mídia DRM em RC4 antes de passá-la para seu aplicativo.

Se o seu aplicativo alterar o tamanho de uma carga ASF durante a transformação, você também deverá remultiplexar o arquivo ASF.

passe para a biblioteca de stub a Windows mídia DRM exportar certificado de aplicativo. O certificado é verificado e, se for válido, o sistema DRM gerará um vetor de inicialização e o criptografará usando o RSA OAEP.

-   Uma chave de sessão RC4 é criada para cada carga concatenando o vetor de inicialização e um valor Salt. Você fornece o valor salt para a API de descriptografia, e você deve incrementar isso por um valor inteiro positivo diferente de zero para cada carga.

você receberá uma ferramenta da Microsoft como parte do contrato de exportação de DRM de mídia Windows que permitirá que você gere seu próprio par de chaves pública/privada RSA. você enviará a chave pública para a microsoft, na qual a microsoft irá incorporá-la em um certificado de aplicativo DRM de mídia Windows assinado e retorná-la.

Cada carga, depois de ser descriptografada usando a chave de descriptografia RC4, deve ser imediatamente criptografada no CPS de saída. há outras restrições sobre o tratamento de cargas não criptografadas que são descritas nas regras de robustez e de conformidade, que acompanham o Windows o contrato de exportação de DRM de mídia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Descriptografia de carga ASF e recriptografação**](asf-payload-decryption-and-re-encryption.md)
</dt> <dt>

[**Exportação de DRM**](drm-export.md)
</dt> <dt>

[**Executando individualização de DRM**](performing-drm-individualization.md)
</dt> <dt>

[**Verificação e inicialização**](verification-and-initialization.md)
</dt> </dl>

 

 




