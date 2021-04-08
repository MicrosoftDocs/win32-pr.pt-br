---
description: Instala um certificado registrado de um arquivo de troca de informações pessoais (PFX) no repositório de certificados.
ms.assetid: f42379d0-b80e-4d95-ab34-9bb35fde06fd
title: installResponseFromPFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db435b3d61f5b2e53a9838024f4080bb8028ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922444"
---
# <a name="installresponsefrompfx"></a>installResponseFromPFX

O exemplo installResponseFromPFX instala um certificado registrado de um arquivo de troca de informações pessoais (PFX) no repositório de certificados.

## <a name="location"></a>Local

Quando você instala o SDK (Software Development Kit) do Microsoft Windows, o exemplo é instalado, por padrão, na pasta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate registro \\ vc \\ installResponseFromPFX.

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

 

 



