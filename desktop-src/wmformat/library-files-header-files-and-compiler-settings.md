---
title: Arquivos de biblioteca, arquivos de cabeçalho e configurações do compilador
description: Arquivos de biblioteca, arquivos de cabeçalho e configurações do compilador
ms.assetid: 7563bb3a-7bea-4e0c-8205-a16b276c8d1e
keywords:
- SDK do Windows Media Format, arquivos de biblioteca DRM
- SDK do Windows Media Format, arquivos de biblioteca
- SDK do Windows Media Format, arquivos de cabeçalho do DRM
- SDK do Windows Media Format, arquivos de cabeçalho
- SDK do Windows Media Format, configurações do compilador do DRM
- SDK do Windows Media Format, configurações do compilador
- DRM (gerenciamento de direitos digitais), arquivos de biblioteca
- DRM (gerenciamento de direitos digitais), arquivos de biblioteca
- DRM (gerenciamento de direitos digitais), arquivos de cabeçalho
- DRM (gerenciamento de direitos digitais), arquivos de cabeçalho
- DRM (gerenciamento de direitos digitais), configurações do compilador
- DRM (gerenciamento de direitos digitais), configurações do compilador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b0b10ea03cc08d5b689b74f9c647f7d0138fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084092"
---
# <a name="library-files-header-files-and-compiler-settings"></a>Arquivos de biblioteca, arquivos de cabeçalho e configurações do compilador

Os componentes de programação das APIs estendidas do cliente DRM do Windows Media são definidos no arquivo de cabeçalho wmdrmsdk. h e implementados nas bibliotecas wmdrmsdk. lib e mfuuid. lib.

Algumas das funcionalidades das APIs estendidas do cliente DRM do Windows Media exigem que você obtenha uma biblioteca protegida da Microsoft. Essa biblioteca, chamada de biblioteca de stub nesta documentação, é específica para o destinatário e especifica o nível de segurança do aplicativo para seus aplicativos. A biblioteca de stub substitui wmdrmsdk. lib; Você nunca deve vincular a ambos.

**Observação** A biblioteca de stubs de DRM é separada da biblioteca de stub usada pelo restante do Windows Media Format SDK, mas é licenciada usando o mesmo método.

**Observação** A biblioteca de stub de DRM deve ser vinculada ao seu aplicativo após o arquivo de biblioteca msvcrt. lib para evitar erros de vinculador.

A biblioteca de stub contém um certificado inserido que pode ser revogado pela Microsoft se você não atender aos termos e condições do contrato de licença.

Métodos específicos que exigem a biblioteca de stub são rotulados na documentação. Se você tentar usar esse método sem vincular à biblioteca de stub, ele retornará um erro STUBLIB do NS \_ E \_ DRM \_ \_ .

O subsistema DRM não pode ser usado em uma compilação de depuração. Se isso for tentado, os métodos da API retornarão o erro de \_ depuração do NS E \_ DRM \_ \_ não \_ permitido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Introdução**](drm-getting-started.md)
</dt> <dt>

[**Arquivos de biblioteca e configurações do compilador**](library-files-and-compiler-settings.md)
</dt> <dt>

[**Obtendo a biblioteca de DRM necessária**](obtaining-the-required-drm-library.md)
</dt> </dl>

 

 




