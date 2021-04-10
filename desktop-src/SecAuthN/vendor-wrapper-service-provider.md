---
description: A finalidade do invólucro do fornecedor é encapsular e usar as interfaces COM de baixo nível (fornecidas pelos fabricantes de cartão inteligente) para um cartão inteligente específico. Essas interfaces não são fornecidas pela Microsoft.
ms.assetid: 7bc26f7b-c355-448a-9f23-4ccfffea2fef
title: Provedor de serviços de wrapper de fornecedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b7d22fea8e450111e1611f2ec069697c229a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090249"
---
# <a name="vendor-wrapper-service-provider"></a><span data-ttu-id="950a4-104">Provedor de serviços de wrapper de fornecedor</span><span class="sxs-lookup"><span data-stu-id="950a4-104">Vendor Wrapper Service Provider</span></span>

<span data-ttu-id="950a4-105">A finalidade do invólucro do fornecedor é encapsular e usar as interfaces COM de baixo nível (fornecidas pelos fabricantes de cartão inteligente) para um cartão inteligente específico.</span><span class="sxs-lookup"><span data-stu-id="950a4-105">The purpose of the vendor wrapper is to encapsulate and use the low-level COM interfaces (supplied by the smart card manufacturers) for a particular smart card.</span></span> <span data-ttu-id="950a4-106">Essas interfaces não são fornecidas pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="950a4-106">These interfaces are not supplied by Microsoft.</span></span>

![invólucro do fornecedor](images/scspart1.png)

<span data-ttu-id="950a4-108">Conforme descrito na parte 6 da *especificação de interoperabilidade para ICCs e sistemas de computadores pessoais* (consulte [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) as especificações em), a funcionalidade exposta por esse wrapper é mais fácil de usar do que a funcionalidade de quatro provedores de serviços separados.</span><span class="sxs-lookup"><span data-stu-id="950a4-108">As described in part 6 of the *Interoperability Specification for ICCs and Personal Computer Systems* (see specifications at [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/)), the functionality exposed by this wrapper is easier to use than the functionality of four separate service providers.</span></span> <span data-ttu-id="950a4-109">A funcionalidade do wrapper pode ser dividida em quatro áreas principais:</span><span class="sxs-lookup"><span data-stu-id="950a4-109">The wrapper's functionality can be divided into four main areas:</span></span>

-   <span data-ttu-id="950a4-110">Serviços de autenticação de cartão inteligente, como obter desafio e autenticação de cartão.</span><span class="sxs-lookup"><span data-stu-id="950a4-110">Smart card authentication services, such as get challenge and card authentication.</span></span>
-   <span data-ttu-id="950a4-111">Acesso a arquivos de cartão inteligente ou serviços do sistema de arquivos, como abrir, fechar, ler e gravar.</span><span class="sxs-lookup"><span data-stu-id="950a4-111">Smart card file access or file system services, such as open, close, read, and write.</span></span>
-   <span data-ttu-id="950a4-112">Gerenciamento de cartão inteligente, como anexar e desanexar.</span><span class="sxs-lookup"><span data-stu-id="950a4-112">Smart card management, such as attach and detach.</span></span>
-   <span data-ttu-id="950a4-113">Serviços de verificação de cartão inteligente, como verificar e alterar código.</span><span class="sxs-lookup"><span data-stu-id="950a4-113">Smart card verification services, such as verify and change code.</span></span>

> [!Note]  
> <span data-ttu-id="950a4-114">Essa especificação pode não estar disponível em alguns idiomas e países ou regiões.</span><span class="sxs-lookup"><span data-stu-id="950a4-114">This specification may not be available in some languages and countries or regions.</span></span>

 

<span data-ttu-id="950a4-115">A funcionalidade é específica para o tipo de cartão que está sendo usado (que funções o cartão dá suporte, protocolos e assim por diante) e será diferente para cada cartão.</span><span class="sxs-lookup"><span data-stu-id="950a4-115">The functionality is specific to the type of card being used (which functions the card supports, protocols, and so on) and will be different for each card.</span></span>

<span data-ttu-id="950a4-116">O wrapper de exemplo do Microsoft SCardCOM usa a biblioteca COM ATL para implementar um wrapper simples e criar um modelo para outros wrappers.</span><span class="sxs-lookup"><span data-stu-id="950a4-116">The Microsoft SCardCOM example wrapper uses the ATL COM library to implement a simple wrapper and lay down a template for other wrappers.</span></span> <span data-ttu-id="950a4-117">Ele implementa as seguintes interfaces.</span><span class="sxs-lookup"><span data-stu-id="950a4-117">It implements the following interfaces.</span></span>



| <span data-ttu-id="950a4-118">Interface ou objeto</span><span class="sxs-lookup"><span data-stu-id="950a4-118">Interface or object</span></span>                                     | <span data-ttu-id="950a4-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="950a4-119">Description</span></span>                         |
|---------------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="950a4-120">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="950a4-120">**ISCardAuth**</span></span>](iscardauth.md)<br/>             | <span data-ttu-id="950a4-121">Serviços de autenticação.</span><span class="sxs-lookup"><span data-stu-id="950a4-121">Authentication services.</span></span><br/> |
| [<span data-ttu-id="950a4-122">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="950a4-122">**ISCardFileAccess**</span></span>](iscardfileaccess.md)<br/> | <span data-ttu-id="950a4-123">Serviços do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="950a4-123">File system services.</span></span><br/>    |
| [<span data-ttu-id="950a4-124">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="950a4-124">**ISCardManage**</span></span>](iscardmanage.md)<br/>         | <span data-ttu-id="950a4-125">Serviços de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="950a4-125">Management services.</span></span><br/>     |
| [<span data-ttu-id="950a4-126">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="950a4-126">**ISCardVerify**</span></span>](iscardverify.md)<br/>         | <span data-ttu-id="950a4-127">Serviços de verificação.</span><span class="sxs-lookup"><span data-stu-id="950a4-127">Verification services.</span></span><br/>   |



 

> [!Note]  
> <span data-ttu-id="950a4-128">O exemplo de SCardCOM é fornecido apenas como um exemplo de implementação das interfaces de wrapper.</span><span class="sxs-lookup"><span data-stu-id="950a4-128">The SCardCOM example is provided only as an example of implementing the wrapper interfaces.</span></span> <span data-ttu-id="950a4-129">Para evitar a colisão de nome de DLL com outros fornecedores, você não deve usar SCardCOM.dll como o nome de qualquer DLL que você criar.</span><span class="sxs-lookup"><span data-stu-id="950a4-129">To prevent DLL name collision with other vendors, you must not use SCardCOM.dll as the name of any DLLs you create.</span></span>

 

<span data-ttu-id="950a4-130">A seguir está um uso típico do wrapper do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="950a4-130">Following is a typical use of the vendor wrapper.</span></span> <span data-ttu-id="950a4-131">Este exemplo usa a interface [**ISCardManage**](iscardmanage.md) para criar instâncias das interfaces que serão encapsuladas no provedor de serviços e na interface [**ISCardVerify**](iscardverify.md) para verificar sua operação.</span><span class="sxs-lookup"><span data-stu-id="950a4-131">This example uses the [**ISCardManage**](iscardmanage.md) interface to create instances of the interfaces that will be wrapped into the service provider and the [**ISCardVerify**](iscardverify.md) interface to verify their operation.</span></span>

<span data-ttu-id="950a4-132">**Para criar um provedor de serviços de wrapper**</span><span class="sxs-lookup"><span data-stu-id="950a4-132">**To build a wrapper service provider**</span></span>

1.  <span data-ttu-id="950a4-133">Crie uma instância da interface [**ISCardManage**](iscardmanage.md) .</span><span class="sxs-lookup"><span data-stu-id="950a4-133">Create an instance of the [**ISCardManage**](iscardmanage.md) interface.</span></span> <span data-ttu-id="950a4-134">Use essa interface para criar uma instância de interfaces necessárias (por exemplo, [**ISCardFileAccess**](iscardfileaccess.md) ou [**ISCardVerify**](iscardverify.md)).</span><span class="sxs-lookup"><span data-stu-id="950a4-134">Use this interface to create an instance of required interfaces (for example, [**ISCardFileAccess**](iscardfileaccess.md) or [**ISCardVerify**](iscardverify.md)).</span></span> <span data-ttu-id="950a4-135">Ao criar essas interfaces, todas as interfaces COM de baixo nível correspondentes também seriam criadas.</span><span class="sxs-lookup"><span data-stu-id="950a4-135">When creating these interfaces, any corresponding low-level COM interfaces would also be created.</span></span>
2.  <span data-ttu-id="950a4-136">Anexe/Conecte-se a um cartão por meio do método [**ISCardManage**](iscardmanage.md) apropriado.</span><span class="sxs-lookup"><span data-stu-id="950a4-136">Attach/connect to a card through the appropriate [**ISCardManage**](iscardmanage.md) method.</span></span>
3.  <span data-ttu-id="950a4-137">Execute as operações necessárias por meio do método [**ISCardVerify**](iscardverify.md) apropriado (que pode chamar várias interfaces com de baixo nível e métodos para concluir).</span><span class="sxs-lookup"><span data-stu-id="950a4-137">Perform required operations through the appropriate [**ISCardVerify**](iscardverify.md) method (which may call multiple low-level COM interfaces and methods to complete).</span></span>
4.  <span data-ttu-id="950a4-138">Repita para outras operações.</span><span class="sxs-lookup"><span data-stu-id="950a4-138">Repeat for other operations.</span></span>
5.  <span data-ttu-id="950a4-139">Liberar ao concluir.</span><span class="sxs-lookup"><span data-stu-id="950a4-139">Release when complete.</span></span>

<span data-ttu-id="950a4-140">O nome da interface COM e o identificador de interface (GUID) não devem ser alterados dos usados no código ou no wrapper de exemplo.</span><span class="sxs-lookup"><span data-stu-id="950a4-140">The COM interface name and interface identifier (GUID) should not change from those used in the code or example wrapper.</span></span> <span data-ttu-id="950a4-141">No entanto, o GUID de classe (ou seja, onde uma implementação real de uma interface reside) deve ser alterado daqueles usados.</span><span class="sxs-lookup"><span data-stu-id="950a4-141">However, the class GUID (that is, where an actual implementation of an interface resides) must be changed from those used.</span></span> <span data-ttu-id="950a4-142">Isso é especialmente importante ao implementar um wrapper de fornecedor.</span><span class="sxs-lookup"><span data-stu-id="950a4-142">This is especially important when implementing a vendor wrapper.</span></span> <span data-ttu-id="950a4-143">Um exemplo seria usar vários wrappers de fornecedor em um computador específico.</span><span class="sxs-lookup"><span data-stu-id="950a4-143">One example would be using multiple vendor wrappers on a particular computer.</span></span> <span data-ttu-id="950a4-144">Esses wrappers devem implementar as mesmas interfaces COM, mas sempre usarão estratégias de implementação diferentes.</span><span class="sxs-lookup"><span data-stu-id="950a4-144">These wrappers should implement the same COM interfaces, but will always use different implementation strategies.</span></span> <span data-ttu-id="950a4-145">Portanto, classes diferentes (e IDs de classe) são necessárias.</span><span class="sxs-lookup"><span data-stu-id="950a4-145">Therefore, different classes (and class IDs) are required.</span></span>

 

 




