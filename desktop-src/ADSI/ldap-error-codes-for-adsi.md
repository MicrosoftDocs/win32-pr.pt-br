---
title: Códigos de erro LDAP para ADSI
description: Quando um servidor LDAP gera um erro e passa o erro para o cliente, o erro é então convertido em uma cadeia de caracteres pelo cliente LDAP.
ms.assetid: 7a0a5a1b-8473-405b-a590-3f917e50cbdc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149abf4562b0e35067149fb69c9a1ec1304cc528
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822202"
---
# <a name="ldap-error-codes-for-adsi"></a><span data-ttu-id="09f0a-103">Códigos de erro LDAP para ADSI</span><span class="sxs-lookup"><span data-stu-id="09f0a-103">LDAP Error Codes for ADSI</span></span>

<span data-ttu-id="09f0a-104">Quando um servidor LDAP gera um erro e passa o erro para o cliente, o erro é então convertido em uma cadeia de caracteres pelo cliente LDAP.</span><span class="sxs-lookup"><span data-stu-id="09f0a-104">When an LDAP server generates an error and passes the error to the client, the error is then translated into a string by the LDAP client.</span></span>

<span data-ttu-id="09f0a-105">Esse método é semelhante aos [códigos de erro do Win32 para ADSI](win32-error-codes-for-adsi.md).</span><span class="sxs-lookup"><span data-stu-id="09f0a-105">This method is similar to [Win32 error codes for ADSI](win32-error-codes-for-adsi.md).</span></span> <span data-ttu-id="09f0a-106">Neste exemplo, o código de erro do cliente é o erro 0x80072020 do WIN32.</span><span class="sxs-lookup"><span data-stu-id="09f0a-106">In this example, the client error code is the WIN32 error 0x80072020.</span></span>

<span data-ttu-id="09f0a-107">**Para determinar os códigos de erro LDAP para ADSI**</span><span class="sxs-lookup"><span data-stu-id="09f0a-107">**To Determine the LDAP error codes for ADSI**</span></span>

1.  <span data-ttu-id="09f0a-108">Descarte o 8007 do código de erro do WIN32.</span><span class="sxs-lookup"><span data-stu-id="09f0a-108">Drop the 8007 from the WIN32 error code.</span></span> <span data-ttu-id="09f0a-109">No exemplo, o valor hexadecimal restante é 2020.</span><span class="sxs-lookup"><span data-stu-id="09f0a-109">In the example, the remaining hex value is 2020.</span></span>
2.  <span data-ttu-id="09f0a-110">Converta o valor hexadecimal restante em um valor decimal.</span><span class="sxs-lookup"><span data-stu-id="09f0a-110">Convert the remaining hex value to a decimal value.</span></span> <span data-ttu-id="09f0a-111">No exemplo, o valor hexadecimal restante 2020 converte para o valor decimal 8224.</span><span class="sxs-lookup"><span data-stu-id="09f0a-111">In the example, the remaining hex value 2020 converts to the decimal value 8224.</span></span>
3.  <span data-ttu-id="09f0a-112">Pesquise no arquivo WinError. h para obter a definição do valor decimal.</span><span class="sxs-lookup"><span data-stu-id="09f0a-112">Search in the WinError.h file for the definition of the decimal value.</span></span> <span data-ttu-id="09f0a-113">No exemplo, 8224L corresponde ao erro de erro **de \_ \_ operações DS \_**.</span><span class="sxs-lookup"><span data-stu-id="09f0a-113">In the example, 8224L corresponds to the error **ERROR\_DS\_OPERATIONS\_ERROR**.</span></span>
4.  <span data-ttu-id="09f0a-114">Substitua o erro de prefixo **\_ DS** por **LDAP \_**.</span><span class="sxs-lookup"><span data-stu-id="09f0a-114">Replace the prefix **ERROR\_DS** with **LDAP\_**.</span></span> <span data-ttu-id="09f0a-115">No exemplo, a nova definição é um **\_ \_ erro de operações LDAP**.</span><span class="sxs-lookup"><span data-stu-id="09f0a-115">In the example, the new definition is **LDAP\_OPERATIONS\_ERROR**.</span></span>
5.  <span data-ttu-id="09f0a-116">Pesquise no arquivo Winldap. h o valor da definição de erro LDAP.</span><span class="sxs-lookup"><span data-stu-id="09f0a-116">Search in the Winldap.h file for the value of the LDAP error definition.</span></span> <span data-ttu-id="09f0a-117">No exemplo, o valor do **erro de \_ operações \_ LDAP** no arquivo Winldap. h é 0x01.</span><span class="sxs-lookup"><span data-stu-id="09f0a-117">In the example, the value of **LDAP\_OPERATIONS\_ERROR** in the Winldap.h file is 0x01.</span></span>

 

 




