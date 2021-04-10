---
title: disable_consistency_check atributo
description: Direciona o RPC para não impor a verificação de consistência de correlação.
ms.assetid: 33ba331d-56e5-4965-a844-7780ea81623d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc55197b5eb680533745a09d4fca4f5827574a7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291951"
---
# <a name="disable_consistency_check-attribute"></a><span data-ttu-id="705d0-103">desabilitar \_ o \_ atributo de verificação de consistência</span><span class="sxs-lookup"><span data-stu-id="705d0-103">disable\_consistency\_check Attribute</span></span>

<span data-ttu-id="705d0-104">Direciona o RPC para não impor a verificação de consistência de correlação.</span><span class="sxs-lookup"><span data-stu-id="705d0-104">Directs RPC to not enforce correlation consistency checking.</span></span>

``` syntax
interface interface-name
{
  return-type function-name(
        [[attribute-list,] disable_consistency_check] param-type param-name
}
```

<span data-ttu-id="705d0-105">Para parâmetros correlacionados, o RPC irá impor que um buffer não nulo seja passado quando a variável de contagem de correlação for não nula.</span><span class="sxs-lookup"><span data-stu-id="705d0-105">For correlated parameters, RPC will enforce that a non-null buffer is passed when the correlation count variable is non-null.</span></span>

## <a name="example"></a><span data-ttu-id="705d0-106">Exemplo</span><span class="sxs-lookup"><span data-stu-id="705d0-106">Example</span></span>

``` syntax
HRESULT PassString( [in] DWORD Length, [in, unique, string, 
    size_is( Length )]LPWSTR MyString );
```

<span data-ttu-id="705d0-107">Se *MyString* for **NULL**, o RPC rejeitará a chamada, a menos que Length esteja definido como 0.</span><span class="sxs-lookup"><span data-stu-id="705d0-107">If *MyString* is **NULL**, RPC will reject the call unless Length is set to 0.</span></span> <span data-ttu-id="705d0-108">Observe que o RPC permitirá que o *comprimento* seja 0 enquanto o *MYSTRING* não for nulo e o RPC tratará *MyString* como uma alocação de buffer de comprimento 0.</span><span class="sxs-lookup"><span data-stu-id="705d0-108">Note that RPC will allow *Length* to be 0 while *MyString* is non-NULL, and RPC will treat *MyString* as a 0-length buffer allocation.</span></span>

## <a name="remarks"></a><span data-ttu-id="705d0-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="705d0-109">Remarks</span></span>

<span data-ttu-id="705d0-110">Para desabilitar essa verificação, a IDL pode conter o \[ \_ atributo Desabilitar verificação de consistência \_ \] em um tipo de parâmetro, typedef ou ponteiro.</span><span class="sxs-lookup"><span data-stu-id="705d0-110">To disable this checking, the IDL can contain the \[disable\_consistency\_check\] attribute on a parameter, typedef, or pointer type.</span></span> <span data-ttu-id="705d0-111">Isso direcionará o RPC para não impor a consistência entre o ponteiro do buffer e a variável de correlação para o buffer apontado pelo parâmetro ou ponteiro.</span><span class="sxs-lookup"><span data-stu-id="705d0-111">This will direct RPC to not enforce the consistency between the buffer pointer and the correlation variable for the buffer pointed to by the parameter or pointer.</span></span>

<span data-ttu-id="705d0-112">Para desabilitar a verificação de consistência de uma compilação de MIDL inteira (e desabilitar a imposição da verificação em todos os casos), a opção de linha de comando MIDL [/Backward \_ compatível com maybenull \_ tamanho](-backward-compat.md) pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="705d0-112">To disable consistency checking for an entire MIDL compilation (and disable enforcement of the checking in all cases), the MIDL command line switch [/backward\_compat maybenull\_sizeis](-backward-compat.md) can be used.</span></span> <span data-ttu-id="705d0-113">Isso exige que o destino da compilação MIDL seja pelo menos â € "Target NT60.</span><span class="sxs-lookup"><span data-stu-id="705d0-113">This requires that the target of the MIDL compilation be at least â€“target NT60.</span></span>

 

 




