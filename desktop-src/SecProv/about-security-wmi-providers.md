---
description: Permitir que os aplicativos interajam com o Trusted Platform Module (TPM) e o Criptografia de Unidade de Disco BitLocker (BDE) por meio da estrutura de gerenciamento unificada do Instrumentação de Gerenciamento do Windows (WMI).
ms.assetid: acd1bc8e-3311-47f9-88b1-739f224e40e9
title: Sobre provedores WMI de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed75cebf14ee3eb419578111b7de15608661d91e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922352"
---
# <a name="about-security-wmi-providers"></a><span data-ttu-id="328f5-103">Sobre provedores WMI de segurança</span><span class="sxs-lookup"><span data-stu-id="328f5-103">About Security WMI Providers</span></span>

<span data-ttu-id="328f5-104">Os provedores de segurança WMI permitem que os aplicativos interajam com o Trusted Platform Module (TPM) e o Criptografia de Unidade de Disco BitLocker (BDE) por meio da estrutura de gerenciamento unificada do Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="328f5-104">The Security WMI Providers allow applications to interact with the Trusted Platform Module (TPM) and BitLocker Drive Encryption (BDE) through the unified management framework of Windows Management Instrumentation (WMI).</span></span>



| <span data-ttu-id="328f5-105">Seção</span><span class="sxs-lookup"><span data-stu-id="328f5-105">Section</span></span>                                                                  | <span data-ttu-id="328f5-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="328f5-106">Description</span></span>                                                                                                                    |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="328f5-107">Referência de provedores WMI de segurança</span><span class="sxs-lookup"><span data-stu-id="328f5-107">Security WMI Providers Reference</span></span>](security-wmi-providers-reference.md) | <span data-ttu-id="328f5-108">Documentação da API para as classes [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) e [**Win32 \_ TPM**](win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="328f5-108">API documentation for [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) and [**Win32\_Tpm**](win32-tpm.md) classes.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="328f5-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="328f5-109">Remarks</span></span>

<span data-ttu-id="328f5-110">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="328f5-110">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="328f5-111">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="328f5-111">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="328f5-112">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="328f5-112">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="328f5-113">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="328f5-113">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

 

 
