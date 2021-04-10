---
description: Um aplicativo pode usar a função RegSetValueEx para associar um valor e seus dados a uma chave. Para obter uma lista dos tipos de valor com suporte em RegSetValueEx, consulte tipos de valor do registro.
ms.assetid: 75ac826a-f169-400c-b6d6-3e3ec9ebf996
title: Gravando e excluindo dados do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5185c98f39a37512ec56fb994d5f1c4ba4b61ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296655"
---
# <a name="writing-and-deleting-registry-data"></a><span data-ttu-id="9817c-104">Gravando e excluindo dados do registro</span><span class="sxs-lookup"><span data-stu-id="9817c-104">Writing and Deleting Registry Data</span></span>

<span data-ttu-id="9817c-105">Um aplicativo pode usar a função [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) para associar um valor e seus dados a uma chave.</span><span class="sxs-lookup"><span data-stu-id="9817c-105">An application can use the [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) function to associate a value and its data with a key.</span></span> <span data-ttu-id="9817c-106">Para obter uma lista dos tipos de valor com suporte em **RegSetValueEx**, consulte [tipos de valor do registro](registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="9817c-106">For a list of the value types supported by **RegSetValueEx**, see [Registry Value Types](registry-value-types.md).</span></span>

<span data-ttu-id="9817c-107">Para excluir um valor de uma chave, um aplicativo pode usar a função [**falha em RegDeleteValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea) .</span><span class="sxs-lookup"><span data-stu-id="9817c-107">To delete a value from a key, an application can use the [**RegDeleteValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea) function.</span></span> <span data-ttu-id="9817c-108">Para excluir uma chave, ela pode usar a função [**RegDeleteKey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) .</span><span class="sxs-lookup"><span data-stu-id="9817c-108">To delete a key, it can use the [**RegDeleteKey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) function.</span></span> <span data-ttu-id="9817c-109">Uma chave excluída não é removida até que o último identificador para ela tenha sido fechado.</span><span class="sxs-lookup"><span data-stu-id="9817c-109">A deleted key is not removed until the last handle to it has been closed.</span></span> <span data-ttu-id="9817c-110">Subchaves e valores não podem ser criados sob uma chave excluída.</span><span class="sxs-lookup"><span data-stu-id="9817c-110">Subkeys and values cannot be created under a deleted key.</span></span>

<span data-ttu-id="9817c-111">Não é possível bloquear uma chave do registro durante uma operação de gravação para sincronizar o acesso aos dados.</span><span class="sxs-lookup"><span data-stu-id="9817c-111">It is not possible to lock a registry key during a write operation to synchronize access to the data.</span></span> <span data-ttu-id="9817c-112">No entanto, você pode controlar o acesso a uma chave do registro usando atributos de segurança.</span><span class="sxs-lookup"><span data-stu-id="9817c-112">However, you can control access to a registry key using security attributes.</span></span> <span data-ttu-id="9817c-113">Para obter mais informações, consulte [segurança da chave do registro e direitos de acesso](registry-key-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="9817c-113">For more information, see [Registry Key Security and Access Rights](registry-key-security-and-access-rights.md).</span></span>

<span data-ttu-id="9817c-114">Mais de uma operação de registro pode ser executada em uma única transação.</span><span class="sxs-lookup"><span data-stu-id="9817c-114">More than one registry operation can be performed within a single transaction.</span></span> <span data-ttu-id="9817c-115">Para associar uma chave do registro a uma transação, um aplicativo pode usar a função [**RegCreateKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda) ou [**RegOpenKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda) .</span><span class="sxs-lookup"><span data-stu-id="9817c-115">To associate a registry key with a transaction, an application can use the [**RegCreateKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda) or [**RegOpenKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda) function.</span></span> <span data-ttu-id="9817c-116">Para obter mais informações sobre transações, consulte [kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal).</span><span class="sxs-lookup"><span data-stu-id="9817c-116">For more information about transactions, see [Kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal).</span></span>

 

 
