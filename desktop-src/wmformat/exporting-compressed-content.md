---
title: Exportando conteúdo compactado
description: Exportando conteúdo compactado
ms.assetid: b312aa5e-d693-4d0a-9d74-b443713cec8c
keywords:
- SDK do Windows Media Format, exportação de DRM
- SDK do Windows Media Format, exportar
- SDK do Windows Media Format, conteúdo compactado
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
ms.openlocfilehash: 37781d5575dbffb7103f07307a149f4bd5e9e4fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822519"
---
# <a name="exporting-compressed-content"></a>Exportando conteúdo compactado

Esta seção descreve como exportar mídia protegida por DRM do Windows Media em um arquivo do Windows Media onde o aplicativo recebe dados de mídia digital compactados. Para fazer isso, seu aplicativo deve executar a descriptografia embutida de todos os conteúdos criptografados do DRM do Windows Media em um arquivo ASF.

> [!Note]  
> Uma biblioteca de análise de ASF é fornecida a você como parte do contrato de exportação do DRM do Windows Media.

 

As principais etapas envolvidas na exportação de conteúdo compactado são:

1.  Execute a individualização de DRM, se necessário.
2.  Verifique se o esquema de proteção de conteúdo de destino é explicitamente permitido.
3.  Crie um objeto de descriptografia para descriptografar cada carga de ASF.
4.  O sistema DRM criptografa cada carga ASF do Windows Media DRM em RC4 antes de passá-la para seu aplicativo.

Se o seu aplicativo alterar o tamanho de uma carga ASF durante a transformação, você também deverá remultiplexar o arquivo ASF.

Passe para a biblioteca de stub um certificado de aplicativo de exportação do Windows Media DRM. O certificado é verificado e, se for válido, o sistema DRM gerará um vetor de inicialização e o criptografará usando o RSA OAEP.

-   Uma chave de sessão RC4 é criada para cada carga concatenando o vetor de inicialização e um valor Salt. Você fornece o valor salt para a API de descriptografia, e você deve incrementar isso por um valor inteiro positivo diferente de zero para cada carga.

Você receberá uma ferramenta da Microsoft como parte do contrato de exportação do DRM do Windows Media que lhe permitirá gerar seu próprio par de chaves pública/privada RSA. Você enviará a chave pública para a Microsoft, na qual a Microsoft irá incorporá-la em um certificado de aplicativo DRM do Windows Media assinado e retorná-la.

Cada carga, depois de ser descriptografada usando a chave de descriptografia RC4, deve ser imediatamente criptografada no CPS de saída. Há outras restrições sobre o tratamento de cargas não criptografadas que são descritas nas regras de robustez e de conformidade, que acompanham o contrato de exportação do DRM do Windows Media.

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

 

 




