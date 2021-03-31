---
title: Códigos de erro do Win32 para ADSI
description: Os códigos de erro padrão do Win32 também são usados para retornar mensagens de erro ADSI.
ms.assetid: 5b7b85c9-ccca-4ea3-8b37-54f6b30a509f
ms.tgt_platform: multiple
keywords:
- Códigos de erro do Win32 para ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a47151a3a1619a7f224dc0b9b7f0871813a346a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634851"
---
# <a name="win32-error-codes-for-adsi"></a><span data-ttu-id="317b1-104">Códigos de erro do Win32 para ADSI</span><span class="sxs-lookup"><span data-stu-id="317b1-104">Win32 Error Codes for ADSI</span></span>

<span data-ttu-id="317b1-105">Os códigos de erro padrão do Win32 também são usados para retornar mensagens de erro ADSI.</span><span class="sxs-lookup"><span data-stu-id="317b1-105">Standard Win32 error codes are also used to return ADSI error messages.</span></span> <span data-ttu-id="317b1-106">Especificamente, o provedor de LDAP ADSI mapeia todos os códigos de erro LDAP para códigos de erro do Win32.</span><span class="sxs-lookup"><span data-stu-id="317b1-106">Specifically, the ADSI LDAP provider maps all the LDAP error codes to Win32 error codes.</span></span> <span data-ttu-id="317b1-107">Os valores **HRESULT** desses códigos de erro são do formato 0x8007XXXX, em que os últimos quatro dígitos hexadecimais, xxxx, correspondem aos valores **DWORD** do código de erro Win32 apropriado.</span><span class="sxs-lookup"><span data-stu-id="317b1-107">The **HRESULT** values of these error codes are of the 0x8007XXXX format, where the last four hexadecimal digits, XXXX, corresponds to the **DWORD** values of the appropriate Win32 error code.</span></span> <span data-ttu-id="317b1-108">Por exemplo, o valor de erro ADSI 0x80072020 fornece o valor de erro Win32 de 0x2020 em hexadecimal ou 8224 em decimal.</span><span class="sxs-lookup"><span data-stu-id="317b1-108">For example, the ADSI error value 0x80072020 gives the Win32 error value of 0x2020 in hexadecimal or 8224 in decimal.</span></span>

<span data-ttu-id="317b1-109">Para converter o valor **HRESULT** de um código de erro ADSI, retornado pelo seu aplicativo, para o valor de **DWORD** de erro do Win32 correspondente, conforme definido nos arquivos de cabeçalho acima, use o procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="317b1-109">To convert the **HRESULT** value of an ADSI error code, returned by your application, to the corresponding the Win32 error **DWORD** value, as defined in the header files above, use the following procedure.</span></span>

<span data-ttu-id="317b1-110">A maioria dos códigos de erro do Win32 para ADSI está definida em Winerror. h ou Lmerr. h.</span><span class="sxs-lookup"><span data-stu-id="317b1-110">Most of the Win32 error codes for ADSI are defined in Winerror.h or Lmerr.h.</span></span> <span data-ttu-id="317b1-111">Os valores de erro são listados como valores decimais nesses arquivos.</span><span class="sxs-lookup"><span data-stu-id="317b1-111">The error values are listed as decimal values in these files.</span></span>

<span data-ttu-id="317b1-112">**Para converter o valor **HRESULT** de um código de erro ADSI para o valor de **DWORD** de erro Win32 correspondente**</span><span class="sxs-lookup"><span data-stu-id="317b1-112">**To convert the **HRESULT** value of an ADSI error code to the corresponding the Win32 error **DWORD** value**</span></span>

1.  <span data-ttu-id="317b1-113">Converta o valor **HRESULT** em um número hexadecimal se estiver começando com um valor decimal, pois você pode obter de um aplicativo Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="317b1-113">Convert the **HRESULT** value to a hexadecimal number if starting with a decimal value as you may get from a Visual Basic application.</span></span>
2.  <span data-ttu-id="317b1-114">Descartar a parte 0x8007 produzir o restante.</span><span class="sxs-lookup"><span data-stu-id="317b1-114">Drop the 0x8007 part produce the remainder.</span></span>
3.  <span data-ttu-id="317b1-115">Converta o resto em um número decimal.</span><span class="sxs-lookup"><span data-stu-id="317b1-115">Convert the remainder to a decimal number.</span></span>
4.  <span data-ttu-id="317b1-116">Pesquisar o restante decimal em Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="317b1-116">Look up the decimal remainder in Winerror.h.</span></span>
5.  <span data-ttu-id="317b1-117">Se não for encontrado em Winerror. h, subtraia 2100 do restante decimal e procure o resultado em Lmerr. h.</span><span class="sxs-lookup"><span data-stu-id="317b1-117">If not found in Winerror.h, subtract 2100 from the decimal remainder and look up the result in Lmerr.h.</span></span>

<span data-ttu-id="317b1-118">O ADSI 2,0 mapeia os códigos de erro LDAP para um conjunto de códigos de erro do Win32 que é diferente daquele usado na ADSI para o Windows 2000 e o cliente DS.</span><span class="sxs-lookup"><span data-stu-id="317b1-118">ADSI 2.0 maps the LDAP error codes to a set of Win32 error codes that is different from that used in ADSI for Windows 2000 and DS Client.</span></span> <span data-ttu-id="317b1-119">As diferenças são listadas em:</span><span class="sxs-lookup"><span data-stu-id="317b1-119">The differences are listed in:</span></span>

-   [<span data-ttu-id="317b1-120">Códigos de erro do Win32</span><span class="sxs-lookup"><span data-stu-id="317b1-120">Win32 Error Codes</span></span>](win32-error-codes.md)
-   [<span data-ttu-id="317b1-121">Códigos de erro do Win32 para ADSI 2,0</span><span class="sxs-lookup"><span data-stu-id="317b1-121">Win32 Error Codes for ADSI 2.0</span></span>](win32-error-codes-for-adsi-2-0.md)

 

 




