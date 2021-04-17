---
description: Registra um computador em uma hierarquia de certificado usando um modelo, um nome de exibição de certificado e a descrição do certificado.
ms.assetid: d9e01767-f6e8-4fd6-a848-8d5acf57407e
title: enrollSimpleMachineCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8582bc73fdee7e8be6b2cff8d0aec81b84487307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813120"
---
# <a name="enrollsimplemachinecert"></a>enrollSimpleMachineCert

O exemplo enrollSimpleMachineCert registra um computador em uma hierarquia de certificado usando um modelo, um nome de exibição de certificado e a descrição do certificado.

## <a name="location"></a>Local

Quando você instala o SDK (Software Development Kit) do Microsoft Windows, uma versão em C++ do exemplo é instalada, por padrão, na pasta *% ProgramFiles%%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate registro \\ vc \\ EnrollSimpleMachineCert. Uma versão do VBScript é instalada no diretório *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enroll \\ \\ EnrollSimpleMachineCert Folder.

## <a name="discussion"></a>Discussão

O exemplo de enrollSimpleMachineCert:

1.  Processa os argumentos de linha de comando. A linha de comando deve conter o nome do modelo, um nome de exibição do certificado e uma descrição do certificado.
2.  Cria um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) e o inicializa usando o modelo especificado na linha de comando. O valor de ContextAdministratorForceMachine do primeiro parâmetro especifica que o certificado está sendo solicitado por um administrador agindo em nome de um computador.
3.  Adiciona o nome de exibição e a descrição ao objeto de registro.
4.  Tenta registrar a solicitação de certificado e verifica o status do processo. A função checkEnrollStatus é definida em enrollCommon. cpp.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando os exemplos incluídos](using-the-included-samples.md)
</dt> </dl>

 

 



