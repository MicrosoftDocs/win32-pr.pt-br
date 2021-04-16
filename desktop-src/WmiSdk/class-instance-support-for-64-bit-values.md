---
description: Fornece restrições para o uso de valores de 64 bits como parte de um caminho.
ms.assetid: 63f4f6c5-7803-425d-912f-bb1dd716e617
ms.tgt_platform: multiple
title: Suporte de instância de classe para valores de 64 bits
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 80f8a48f253cf2ef1902938ca6c54d01404b8466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757662"
---
# <a name="class-instance-support-for-64-bit-values"></a><span data-ttu-id="915c0-103">Suporte de instância de classe para valores de 64 bits</span><span class="sxs-lookup"><span data-stu-id="915c0-103">Class Instance Support for 64-Bit Values</span></span>

<span data-ttu-id="915c0-104">Você pode usar um valor de chave de 64 bits como parte de um caminho, com as seguintes restrições:</span><span class="sxs-lookup"><span data-stu-id="915c0-104">You can use a 64-bit key value as part of a path, with the following restrictions:</span></span>

-   <span data-ttu-id="915c0-105">Desde que você não exceda o intervalo de 32 bits, você pode atribuir e recuperar valores da chave como faria com uma propriedade de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="915c0-105">As long as you do not exceed the 32-bit range, you can assign and retrieve values from the key as you would a 32-bit property.</span></span>
-   <span data-ttu-id="915c0-106">Depois de exceder o valor inteiro de 0x7FFFFFFF (para tipos assinados), 0x80000000 (para tipos não assinados) ou 32 bits, você deve usar aspas.</span><span class="sxs-lookup"><span data-stu-id="915c0-106">After you exceed the integer value of 0x7FFFFFFF (for signed types), 0x80000000 (for unsigned types), or 32 bits, you must use quotation marks.</span></span>
-   <span data-ttu-id="915c0-107">O único caminho válido para um valor de 64 bits está localizado nas propriedades **\_ \_ RelPath** ou **\_ \_ Path** da instância.</span><span class="sxs-lookup"><span data-stu-id="915c0-107">The only valid path for a 64-bit value is located in the **\_\_RELPATH** or **\_\_PATH** properties of the instance.</span></span> <span data-ttu-id="915c0-108">Como tal, o WMI não oferece suporte à notação hexadecimal para o valor equivalente.</span><span class="sxs-lookup"><span data-stu-id="915c0-108">As such, WMI does not support the hexadecimal notation for the equivalent value.</span></span>
-   <span data-ttu-id="915c0-109">Se o WMI registra a chave de instância como um número negativo, você deve usar o número original para recuperar a instância.</span><span class="sxs-lookup"><span data-stu-id="915c0-109">If WMI records the instance key as a negative number, then you must use the original number to retrieve the instance.</span></span>

<span data-ttu-id="915c0-110">A semântica de consulta não é afetada e se comporta conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="915c0-110">Query semantics are unaffected and behave as expected.</span></span> <span data-ttu-id="915c0-111">Esse comportamento afeta apenas as operações caminho do objeto, [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)e [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .</span><span class="sxs-lookup"><span data-stu-id="915c0-111">This behavior only affects the object path, [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), and [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) operations.</span></span>

<span data-ttu-id="915c0-112">O exemplo a seguir mostra que as instâncias de classe podem ter valores de chave de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="915c0-112">The following example shows that class instances can have 64-bit key values.</span></span>

``` syntax
class MyBig
{
  [key] sint64 k;
  sint64 p;
};

instance of MyBig
{
  k = 2;
  p = 3;
};
```

 

 



