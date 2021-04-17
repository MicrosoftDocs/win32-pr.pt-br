---
description: A interface INonDelegatingUnknown é uma versão de IUnknown que é renomeada para habilitar o suporte para interfaces de não delegação e de delegação de interface IUnknown no mesmo objeto COM.
ms.assetid: a2faf9d1-2130-4c6c-8fcd-3e118d592b7f
title: INonDelegatingUnknown (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INonDelegatingUnknown
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13e93d5ba083706ee361addeb4db2157471cbe25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775602"
---
# <a name="inondelegatingunknown"></a><span data-ttu-id="aecc8-103">INonDelegatingUnknown</span><span class="sxs-lookup"><span data-stu-id="aecc8-103">INonDelegatingUnknown</span></span>

<span data-ttu-id="aecc8-104">A `INonDelegatingUnknown` interface é uma versão de **IUnknown** renomeada para habilitar o suporte para interfaces de não delegação e de delegação de interface **IUnknown** no mesmo objeto com.</span><span class="sxs-lookup"><span data-stu-id="aecc8-104">The `INonDelegatingUnknown` interface is a version of **IUnknown** that is renamed to enable support for both nondelegating and delegating **IUnknown** interfaces in the same COM object.</span></span>

## <a name="syntax"></a><span data-ttu-id="aecc8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aecc8-105">Syntax</span></span>


```C++
interface INonDelegatingUnknown
{
    virtual HRESULT NonDelegatingQueryInterface) (REFIID riid, LPVOID *ppv) PURE;
    virtual ULONG NonDelegatingAddRef)(void) PURE;
    virtual ULONG NonDelegatingRelease)(void) PURE;
};
```



## <a name="remarks"></a><span data-ttu-id="aecc8-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="aecc8-106">Remarks</span></span>

<span data-ttu-id="aecc8-107">Para usar `INonDelegatingUnknown` para várias heranças, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="aecc8-107">To use `INonDelegatingUnknown` for multiple inheritance, perform the following steps.</span></span>

1.  <span data-ttu-id="aecc8-108">Derive sua classe de uma interface, por exemplo, IMinhaInterface.</span><span class="sxs-lookup"><span data-stu-id="aecc8-108">Derive your class from an interface, for example, IMyInterface.</span></span>
2.  <span data-ttu-id="aecc8-109">Inclua [**Declare \_ IUnknown**](declare-iunknown.md) em sua definição de classe para declarar implementações de **QueryInterface**, **AddRef** e **Release** que chamam o desconhecido externo.</span><span class="sxs-lookup"><span data-stu-id="aecc8-109">Include [**DECLARE\_IUNKNOWN**](declare-iunknown.md) in your class definition to declare implementations of **QueryInterface**, **AddRef**, and **Release** that call the outer unknown.</span></span>
3.  <span data-ttu-id="aecc8-110">Substitua **NonDelegatingQueryInterface** para expor IMinhaInterface com código como o seguinte:</span><span class="sxs-lookup"><span data-stu-id="aecc8-110">Override **NonDelegatingQueryInterface** to expose IMyInterface with code such as the following:</span></span>
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  <span data-ttu-id="aecc8-111">Declare e implemente as funções de membro de IMinhaInterface.</span><span class="sxs-lookup"><span data-stu-id="aecc8-111">Declare and implement the member functions of IMyInterface.</span></span>

<span data-ttu-id="aecc8-112">Para usar `INonDelegatingUnknown` o para interfaces aninhadas, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="aecc8-112">To use `INonDelegatingUnknown` for nested interfaces, perform the following steps:</span></span>

1.  <span data-ttu-id="aecc8-113">Declare uma classe derivada de [**CUnknown**](cunknown.md).</span><span class="sxs-lookup"><span data-stu-id="aecc8-113">Declare a class derived from [**CUnknown**](cunknown.md).</span></span>
2.  <span data-ttu-id="aecc8-114">Inclua [**Declare \_ IUnknown**](declare-iunknown.md) em sua definição de classe.</span><span class="sxs-lookup"><span data-stu-id="aecc8-114">Include [**DECLARE\_IUNKNOWN**](declare-iunknown.md) in your class definition.</span></span>
3.  <span data-ttu-id="aecc8-115">Substitua **NonDelegatingQueryInterface** para expor IMinhaInterface com o código como o seguinte:</span><span class="sxs-lookup"><span data-stu-id="aecc8-115">Override **NonDelegatingQueryInterface** to expose IMyInterface with the code such as the following:</span></span>
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  <span data-ttu-id="aecc8-116">Implemente as funções de membro de IMinhaInterface.</span><span class="sxs-lookup"><span data-stu-id="aecc8-116">Implement the member functions of IMyInterface.</span></span> <span data-ttu-id="aecc8-117">Use [**CUnknown:: GetOwner**](cunknown-getowner.md) para acessar a classe de objeto com.</span><span class="sxs-lookup"><span data-stu-id="aecc8-117">Use [**CUnknown::GetOwner**](cunknown-getowner.md) to access the COM object class.</span></span>
5.  <span data-ttu-id="aecc8-118">Em sua classe de objeto COM, torne a classe aninhada um amigo da classe de objeto COM e declare uma instância da classe aninhada como um membro da classe de objeto COM.</span><span class="sxs-lookup"><span data-stu-id="aecc8-118">In your COM object class, make the nested class a friend of the COM object class, and declare an instance of the nested class as a member of the COM object class.</span></span>

<span data-ttu-id="aecc8-119">Como você sempre deve passar o desconhecido externo e um **HRESULT** para o construtor [**CUnknown**](cunknown.md) , não é possível usar um construtor padrão.</span><span class="sxs-lookup"><span data-stu-id="aecc8-119">Because you must always pass the outer unknown and an **HRESULT** to the [**CUnknown**](cunknown.md) constructor, you can't use a default constructor.</span></span> <span data-ttu-id="aecc8-120">Você precisa tornar a variável de membro um ponteiro para a classe e fazer uma nova chamada em seu construtor para realmente criá-la.</span><span class="sxs-lookup"><span data-stu-id="aecc8-120">You have to make the member variable a pointer to the class and make a new call in your constructor to actually create it.</span></span>

<span data-ttu-id="aecc8-121">Substitua o **NonDelegatingQueryInterface** por um código como o seguinte:</span><span class="sxs-lookup"><span data-stu-id="aecc8-121">Override the **NonDelegatingQueryInterface** with code such as the following:</span></span>


```C++
     if (riid == IID_IMyInterface) {
         return m_pImplFilter->
            NonDelegatingQueryInterface(IID_IMyInterface, ppv);
     } else {
         return CUnknown::NonDelegatingQueryInterface(riid, ppv);
     }
```



<span data-ttu-id="aecc8-122">Você pode ter classes mistas que dão suporte a algumas interfaces por meio de várias heranças e algumas interfaces por meio de classes aninhadas.</span><span class="sxs-lookup"><span data-stu-id="aecc8-122">You can have mixed classes that support some interfaces through multiple inheritance and some interfaces through nested classes.</span></span>

## <a name="requirements"></a><span data-ttu-id="aecc8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aecc8-123">Requirements</span></span>



| <span data-ttu-id="aecc8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="aecc8-124">Requirement</span></span> | <span data-ttu-id="aecc8-125">Valor</span><span class="sxs-lookup"><span data-stu-id="aecc8-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aecc8-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aecc8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="aecc8-127"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aecc8-127"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="aecc8-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aecc8-128">Library</span></span><br/> | <dl> <span data-ttu-id="aecc8-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="aecc8-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aecc8-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="aecc8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aecc8-131">**Funções auxiliares COM**</span><span class="sxs-lookup"><span data-stu-id="aecc8-131">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> </dl>

 

 




