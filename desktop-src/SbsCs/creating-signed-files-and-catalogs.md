---
description: Para assinar um arquivo e criar um catálogo para ele, você deve primeiro ter um processo para assinar arquivos, um certificado e uma chave pública.
ms.assetid: 61337ea6-2d6b-4080-9128-5b8527512ce6
title: Criando arquivos e catálogos assinados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9abcccc2451cfa9461bc8129705c1094291b33fea609679c89ef46d7cf7348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142319"
---
# <a name="creating-signed-files-and-catalogs"></a>Criando arquivos e catálogos assinados

Para assinar um arquivo e criar um catálogo para ele, você deve primeiro ter um processo para assinar arquivos, um certificado e uma chave pública.

**Para assinar um arquivo e criar um catálogo**

1.  Use [Pktextract.exe](pktextract-exe.md) para extrair o [*token de chave pública*](p-sbscs-gly.md) do arquivo de certificado. O arquivo de certificado deve estar presente no mesmo diretório que o utilitário.
2.  Use o valor do token de chave pública para atualizar o atributo **PublicKeyToken** do elemento **AssemblyIdentity** no arquivo de manifesto.
3.  Use [MT.exe](mt-exe.md) para gerar hashes de arquivos contidos no manifesto do assembly e para criar o arquivo de descrição do catálogo (. CDF).
4.  Use Makecat.exe com o. CDF gerado para criar o catálogo de segurança para o assembly. Essa ferramenta está incluída no CryptoAPI.
5.  Use o utilitário [SignTool](/windows/desktop/SecCrypto/signtool) para assinar o catálogo gerado com o certificado usado na etapa 1. O. CDF das etapas 3 e 4 pode ser excluído depois que o catálogo é criado.

Consulte também o [exemplo de assinatura de assembly](assembly-signing-example.md).

 

 
