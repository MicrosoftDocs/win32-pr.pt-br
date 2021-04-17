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
# <a name="enrollsimplemachinecert"></a><span data-ttu-id="159df-103">enrollSimpleMachineCert</span><span class="sxs-lookup"><span data-stu-id="159df-103">enrollSimpleMachineCert</span></span>

<span data-ttu-id="159df-104">O exemplo enrollSimpleMachineCert registra um computador em uma hierarquia de certificado usando um modelo, um nome de exibição de certificado e a descrição do certificado.</span><span class="sxs-lookup"><span data-stu-id="159df-104">The enrollSimpleMachineCert sample enrolls a computer in a certificate hierarchy by using a template, a certificate display name, and the certificate description.</span></span>

## <a name="location"></a><span data-ttu-id="159df-105">Local</span><span class="sxs-lookup"><span data-stu-id="159df-105">Location</span></span>

<span data-ttu-id="159df-106">Quando você instala o SDK (Software Development Kit) do Microsoft Windows, uma versão em C++ do exemplo é instalada, por padrão, na pasta *% ProgramFiles%%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate registro \\ vc \\ EnrollSimpleMachineCert.</span><span class="sxs-lookup"><span data-stu-id="159df-106">When you install the Microsoft Windows Software Development Kit (SDK), a C++ version of the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\EnrollSimpleMachineCert folder.</span></span> <span data-ttu-id="159df-107">Uma versão do VBScript é instalada no diretório *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enroll \\ \\ EnrollSimpleMachineCert Folder.</span><span class="sxs-lookup"><span data-stu-id="159df-107">A VBScript version is installed in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VBS\\EnrollSimpleMachineCert folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="159df-108">Discussão</span><span class="sxs-lookup"><span data-stu-id="159df-108">Discussion</span></span>

<span data-ttu-id="159df-109">O exemplo de enrollSimpleMachineCert:</span><span class="sxs-lookup"><span data-stu-id="159df-109">The enrollSimpleMachineCert sample:</span></span>

1.  <span data-ttu-id="159df-110">Processa os argumentos de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="159df-110">Processes the command line arguments.</span></span> <span data-ttu-id="159df-111">A linha de comando deve conter o nome do modelo, um nome de exibição do certificado e uma descrição do certificado.</span><span class="sxs-lookup"><span data-stu-id="159df-111">The command line should contain the name of the template, a certificate display name, and a certificate description.</span></span>
2.  <span data-ttu-id="159df-112">Cria um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) e o inicializa usando o modelo especificado na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="159df-112">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object and initializes it by using the template specified on the command line.</span></span> <span data-ttu-id="159df-113">O valor de ContextAdministratorForceMachine do primeiro parâmetro especifica que o certificado está sendo solicitado por um administrador agindo em nome de um computador.</span><span class="sxs-lookup"><span data-stu-id="159df-113">The ContextAdministratorForceMachine value for the first parameter specifies that the certificate is being requested by an administrator acting on behalf of a computer.</span></span>
3.  <span data-ttu-id="159df-114">Adiciona o nome de exibição e a descrição ao objeto de registro.</span><span class="sxs-lookup"><span data-stu-id="159df-114">Adds the display name and description to the enrollment object.</span></span>
4.  <span data-ttu-id="159df-115">Tenta registrar a solicitação de certificado e verifica o status do processo.</span><span class="sxs-lookup"><span data-stu-id="159df-115">Attempts to enroll the certificate request and checks the status of the process.</span></span> <span data-ttu-id="159df-116">A função checkEnrollStatus é definida em enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="159df-116">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="159df-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="159df-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="159df-118">Usando os exemplos incluídos</span><span class="sxs-lookup"><span data-stu-id="159df-118">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



