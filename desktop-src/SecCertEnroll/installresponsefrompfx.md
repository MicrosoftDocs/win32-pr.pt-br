---
description: instala um certificado registrado de um arquivo Exchange de informações pessoais (PFX) no repositório de certificados.
ms.assetid: f42379d0-b80e-4d95-ab34-9bb35fde06fd
title: installResponseFromPFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540e719f098d227afac4af59fd2d296d9d06606d04b9de80cf1e24081918d6f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117777602"
---
# <a name="installresponsefrompfx"></a>installResponseFromPFX

o exemplo installResponseFromPFX instala um certificado registrado de um arquivo de Exchange informações pessoais (PFX) para o repositório de certificados.

## <a name="location"></a>Localização

quando você instala o Microsoft Windows Software Development Kit (SDK), o exemplo é instalado, por padrão, na pasta *% programfiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ samples \\ Security \\ X509 Certificate registro \\ VC \\ installResponseFromPFX.

## <a name="discussion"></a>Discussão

O exemplo de installResponseFromPFX:

1.  Processa os argumentos de linha de comando. A linha de comando deve conter:
    -   O nome do exemplo.
    -   O nome do arquivo PFX que contém o certificado registrado.
    -   Uma senha associada ao arquivo PFX.
2.  Lê o arquivo PFX, experimentando o formato Base64 primeiro e o formato binário se a base64 falhar. A função DecodeFileW () é definida em enrollCommon. cpp.
3.  Converte o certificado registrado em um **BSTR** e o usa para inicializar um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) . A função convertWszToBstr é definida em enrollCommon. cpp.
4.  Instala o certificado no repositório de certificados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[enrollEOBOCMC](enrolleobocmc.md)
</dt> <dt>

[Usando os exemplos incluídos](using-the-included-samples.md)
</dt> </dl>

 

 



