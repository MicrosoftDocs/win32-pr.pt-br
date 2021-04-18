---
description: As interfaces a seguir podem ser usadas para registrar um usuário ou um computador em uma hierarquia de certificado.
ms.assetid: 653bc971-8bda-4e23-a56a-dbeb36eeaf6d
title: Interfaces de registro de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e13e8db7d2938b7facb0b055303c1bdc18392a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760213"
---
# <a name="certificate-enrollment-interfaces"></a><span data-ttu-id="e15ed-103">Interfaces de registro de certificado</span><span class="sxs-lookup"><span data-stu-id="e15ed-103">Certificate Enrollment Interfaces</span></span>

<span data-ttu-id="e15ed-104">As interfaces a seguir podem ser usadas para registrar um usuário ou um computador em uma hierarquia de certificado.</span><span class="sxs-lookup"><span data-stu-id="e15ed-104">The following interfaces can be used to enroll a user or a computer in a certificate hierarchy.</span></span>



| <span data-ttu-id="e15ed-105">Interface</span><span class="sxs-lookup"><span data-stu-id="e15ed-105">Interface</span></span>                                              | <span data-ttu-id="e15ed-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="e15ed-106">Description</span></span>                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e15ed-107">**IX509Enrollment**</span><span class="sxs-lookup"><span data-stu-id="e15ed-107">**IX509Enrollment**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)             | <span data-ttu-id="e15ed-108">Registra um computador ou usuário em uma hierarquia de certificado.</span><span class="sxs-lookup"><span data-stu-id="e15ed-108">Enrolls a computer or user in a certificate hierarchy.</span></span>                                                                                                                              |
| [<span data-ttu-id="e15ed-109">**IX509Enrollment2**</span><span class="sxs-lookup"><span data-stu-id="e15ed-109">**IX509Enrollment2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollment2)           | <span data-ttu-id="e15ed-110">Estende a interface [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para habilitar a inicialização a partir de um modelo.</span><span class="sxs-lookup"><span data-stu-id="e15ed-110">Extends the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) interface to enable initialization from a template.</span></span>                                                                          |
| [<span data-ttu-id="e15ed-111">**IX509EnrollmentHelper**</span><span class="sxs-lookup"><span data-stu-id="e15ed-111">**IX509EnrollmentHelper**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollmenthelper) | <span data-ttu-id="e15ed-112">Define métodos que permitem que um aplicativo Web registre um certificado, armazene as credenciais do servidor de política no cache de credenciais e registre servidores de política e servidores de registro.</span><span class="sxs-lookup"><span data-stu-id="e15ed-112">Defines methods that enable a web application to enroll a certificate, store policy server credentials in the credential cache, and register policy servers and enrollment servers.</span></span> |
| [<span data-ttu-id="e15ed-113">**IX509EnrollmentStatus**</span><span class="sxs-lookup"><span data-stu-id="e15ed-113">**IX509EnrollmentStatus**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) | <span data-ttu-id="e15ed-114">Recupera informações detalhadas de erro sobre uma transação de registro de certificado.</span><span class="sxs-lookup"><span data-stu-id="e15ed-114">Retrieves detailed error information about a certificate enrollment transaction.</span></span>                                                                                                    |
| [<span data-ttu-id="e15ed-115">**IX509SCEPEnrollment**</span><span class="sxs-lookup"><span data-stu-id="e15ed-115">**IX509SCEPEnrollment**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment)     | <span data-ttu-id="e15ed-116">Interface de protocolo de registro de computador simples X. 509</span><span class="sxs-lookup"><span data-stu-id="e15ed-116">X.509 Simple Computer Enrollment Protocol Interface</span></span><br/>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="e15ed-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e15ed-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e15ed-118">Interfaces CertEnroll</span><span class="sxs-lookup"><span data-stu-id="e15ed-118">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 




