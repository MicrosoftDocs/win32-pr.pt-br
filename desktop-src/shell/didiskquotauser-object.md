---
description: Permite que um cliente gerencie as configurações de cota de disco global de um volume NTFS. Esse objeto disponibiliza a funcionalidade essencial da interface DIDiskQuotaUser para scripts e aplicativos baseados Visual Basic Microsoft.
title: Objeto DIDiskQuotaUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0cdf3293-3dcf-44e7-a80d-4eacf9d09fbf
ms.openlocfilehash: b370056f40320561a38b1f77fbcf9a53ee35686a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843237"
---
# <a name="didiskquotauser-object"></a><span data-ttu-id="30002-104">Objeto DIDiskQuotaUser</span><span class="sxs-lookup"><span data-stu-id="30002-104">DIDiskQuotaUser object</span></span>

<span data-ttu-id="30002-105">Permite que um cliente gerencie as configurações de cota de disco global de um volume NTFS.</span><span class="sxs-lookup"><span data-stu-id="30002-105">Allows a client to manage an NTFS volume's global disk quota settings.</span></span> <span data-ttu-id="30002-106">Esse objeto disponibiliza a funcionalidade essencial da interface **DIDiskQuotaUser** para scripts e aplicativos baseados Visual Basic Microsoft.</span><span class="sxs-lookup"><span data-stu-id="30002-106">This object makes the essential functionality of the **DIDiskQuotaUser** interface available to scripting and Microsoft Visual Basic-based applications.</span></span>

## <a name="members"></a><span data-ttu-id="30002-107">Membros</span><span class="sxs-lookup"><span data-stu-id="30002-107">Members</span></span>

<span data-ttu-id="30002-108">O **objeto DIDiskQuotaUser** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="30002-108">The **DIDiskQuotaUser** object has these types of members:</span></span>

-   [<span data-ttu-id="30002-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="30002-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="30002-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="30002-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="30002-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="30002-111">Methods</span></span>

<span data-ttu-id="30002-112">O **objeto DIDiskQuotaUser** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="30002-112">The **DIDiskQuotaUser** object has these methods.</span></span>



| <span data-ttu-id="30002-113">Método</span><span class="sxs-lookup"><span data-stu-id="30002-113">Method</span></span>                                           | <span data-ttu-id="30002-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="30002-114">Description</span></span>                                             |
|:-------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="30002-115">**Invalidate**</span><span class="sxs-lookup"><span data-stu-id="30002-115">**Invalidate**</span></span>](didiskquotauser-invalidate.md) | <span data-ttu-id="30002-116">Limpa as informações de usuário armazenadas em cache do objeto.</span><span class="sxs-lookup"><span data-stu-id="30002-116">Clears the object's cached user information.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="30002-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="30002-117">Properties</span></span>

<span data-ttu-id="30002-118">O **objeto DIDiskQuotaUser** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="30002-118">The **DIDiskQuotaUser** object has these properties.</span></span>



| <span data-ttu-id="30002-119">Propriedade</span><span class="sxs-lookup"><span data-stu-id="30002-119">Property</span></span>                                                                        | <span data-ttu-id="30002-120">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="30002-120">Access type</span></span>           | <span data-ttu-id="30002-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="30002-121">Description</span></span>                                                                                          |
|:--------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30002-122">**AccountContainerName**</span><span class="sxs-lookup"><span data-stu-id="30002-122">**AccountContainerName**</span></span>](didiskquotauser-accountcontainername.md)<br/> | <span data-ttu-id="30002-123">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30002-123">Read-only</span></span><br/>  | <span data-ttu-id="30002-124">Obtém o nome do contêiner da conta do usuário.</span><span class="sxs-lookup"><span data-stu-id="30002-124">Gets the name of the user's account container.</span></span><br/>                                            |
| [<span data-ttu-id="30002-125">**AccountStatus**</span><span class="sxs-lookup"><span data-stu-id="30002-125">**AccountStatus**</span></span>](didiskquotauser-accountstatus.md)<br/>               | <span data-ttu-id="30002-126">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30002-126">Read-only</span></span><br/>  | <span data-ttu-id="30002-127">Obtém o status da conta do usuário.</span><span class="sxs-lookup"><span data-stu-id="30002-127">Gets the status of the user's account.</span></span><br/>                                                    |
| [<span data-ttu-id="30002-128">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="30002-128">**DisplayName**</span></span>](didiskquotauser-displayname.md)<br/>                   | <span data-ttu-id="30002-129">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30002-129">Read-only</span></span><br/>  | <span data-ttu-id="30002-130">Obtém o nome de exibição do usuário.</span><span class="sxs-lookup"><span data-stu-id="30002-130">Gets the user's display name.</span></span><br/>                                                             |
| [<span data-ttu-id="30002-131">**ID**</span><span class="sxs-lookup"><span data-stu-id="30002-131">**ID**</span></span>](didiskquotauser-id.md)<br/>                                     | <span data-ttu-id="30002-132">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30002-132">Read-only</span></span><br/>  | <span data-ttu-id="30002-133">Obtém uma ID que identifica exclusivamente o usuário.</span><span class="sxs-lookup"><span data-stu-id="30002-133">Gets an ID that uniquely identifies the user.</span></span><br/>                                             |
| [<span data-ttu-id="30002-134">**LogonName**</span><span class="sxs-lookup"><span data-stu-id="30002-134">**LogonName**</span></span>](didiskquotauser-logonname.md)<br/>                       | <span data-ttu-id="30002-135">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30002-135">Read-only</span></span><br/>  | <span data-ttu-id="30002-136">Obtém o nome da conta de logon do usuário.</span><span class="sxs-lookup"><span data-stu-id="30002-136">Gets the user's logon account name.</span></span><br/>                                                       |
| [<span data-ttu-id="30002-137">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="30002-137">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)<br/>                     | <span data-ttu-id="30002-138">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="30002-138">Read/write</span></span><br/> | <span data-ttu-id="30002-139">Define ou obtém o limite de cota [**atual do usuário.**](diskquotacontrol-object.md)</span><span class="sxs-lookup"><span data-stu-id="30002-139">Sets or gets the user's current [**quota limit**](diskquotacontrol-object.md).</span></span><br/>           |
| [<span data-ttu-id="30002-140">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="30002-140">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)<br/>             | <span data-ttu-id="30002-141">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30002-141">Read-only</span></span><br/>  | <span data-ttu-id="30002-142">Obtém o [**limite de cota**](diskquotacontrol-object.md) atual do usuário como uma cadeia de texto.</span><span class="sxs-lookup"><span data-stu-id="30002-142">Gets the user's current [**quota limit**](diskquotacontrol-object.md) as a text string.</span></span> <br/> |
| [<span data-ttu-id="30002-143">**QuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="30002-143">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)<br/>             | <span data-ttu-id="30002-144">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="30002-144">Read/write</span></span><br/> | <span data-ttu-id="30002-145">Define ou Obtém o limite de aviso do usuário, em bytes.</span><span class="sxs-lookup"><span data-stu-id="30002-145">Sets or gets the user's warning threshold, in bytes.</span></span><br/>                                      |
| [<span data-ttu-id="30002-146">**QuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="30002-146">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)<br/>     | <span data-ttu-id="30002-147">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30002-147">Read-only</span></span><br/>  | <span data-ttu-id="30002-148">Obtém o limite de aviso do usuário como uma cadeia de texto.</span><span class="sxs-lookup"><span data-stu-id="30002-148">Gets the user's warning threshold as a text string.</span></span><br/>                                       |
| [<span data-ttu-id="30002-149">**QuotaUsed**</span><span class="sxs-lookup"><span data-stu-id="30002-149">**QuotaUsed**</span></span>](didiskquotauser-quotaused.md)<br/>                       | <span data-ttu-id="30002-150">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30002-150">Read-only</span></span><br/>  | <span data-ttu-id="30002-151">Obtém o uso do disco atual do usuário, em bytes.</span><span class="sxs-lookup"><span data-stu-id="30002-151">Gets the user's current disk usage, in bytes.</span></span><br/>                                             |
| [<span data-ttu-id="30002-152">**QuotaUsedText**</span><span class="sxs-lookup"><span data-stu-id="30002-152">**QuotaUsedText**</span></span>](didiskquotauser-quotausedtext.md)<br/>               | <span data-ttu-id="30002-153">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30002-153">Read-only</span></span><br/>  | <span data-ttu-id="30002-154">Obtém o uso do disco atual do usuário como uma cadeia de texto.</span><span class="sxs-lookup"><span data-stu-id="30002-154">Gets the user's current disk usage as a text string.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="30002-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="30002-155">Remarks</span></span>

<span data-ttu-id="30002-156">Cada usuário no volume que é gerenciado pelo objeto [**DiskQuotaControl**](diskquotacontrol-object.md) tem um objeto **DIDiskQuotaUser** associado a ele.</span><span class="sxs-lookup"><span data-stu-id="30002-156">Each user on the volume that is managed by the [**DiskQuotaControl**](diskquotacontrol-object.md) object has a **DIDiskQuotaUser** object associated with it.</span></span> <span data-ttu-id="30002-157">Esse objeto permite que um cliente gerencie as configurações de um usuário individual.</span><span class="sxs-lookup"><span data-stu-id="30002-157">This object allows a client to manage an individual user's settings.</span></span> <span data-ttu-id="30002-158">Há várias maneiras de obter o objeto **DIDiskQuotaUser** de um usuário:</span><span class="sxs-lookup"><span data-stu-id="30002-158">There are several ways to obtain a user's **DIDiskQuotaUser** object:</span></span>

-   <span data-ttu-id="30002-159">Os objetos **DIDiskQuotaUser** para todos os usuários com cotas no volume são expostos como uma coleção e podem ser enumerados.</span><span class="sxs-lookup"><span data-stu-id="30002-159">The **DIDiskQuotaUser** objects for all users with quotas on the volume are exposed as a collection and can be enumerated.</span></span> <span data-ttu-id="30002-160">Uma discussão sobre como enumerar objetos **DIDiskQuotaUser** é encontrada abaixo.</span><span class="sxs-lookup"><span data-stu-id="30002-160">A discussion of how to enumerate **DIDiskQuotaUser** objects is found below.</span></span>
-   <span data-ttu-id="30002-161">Quando você adiciona um novo usuário, o método [**adduser**](diskquotacontrol-adduser.md) retorna o objeto **DIDiskQuotaUser** do usuário.</span><span class="sxs-lookup"><span data-stu-id="30002-161">When you add a new user, the [**AddUser**](diskquotacontrol-adduser.md) method returns the user's **DIDiskQuotaUser** object.</span></span>
-   <span data-ttu-id="30002-162">Se você tiver o nome do usuário, o método [**FindUser**](diskquotacontrol-finduser.md) retornará o objeto **DIDiskQuotaUser** do usuário.</span><span class="sxs-lookup"><span data-stu-id="30002-162">If you have the user's name, the [**FindUser**](diskquotacontrol-finduser.md) method returns the user's **DIDiskQuotaUser** object.</span></span>

### <a name="enumerating-disk-quota-users"></a><span data-ttu-id="30002-163">Enumerando usuários de cota de disco</span><span class="sxs-lookup"><span data-stu-id="30002-163">Enumerating Disk Quota Users</span></span>

<span data-ttu-id="30002-164">Os objetos **DIDiskQuotaUser** para todos os usuários com uma cota no volume são expostos como uma coleção.</span><span class="sxs-lookup"><span data-stu-id="30002-164">The **DIDiskQuotaUser** objects for all users with a quota on the volume are exposed as a collection.</span></span> <span data-ttu-id="30002-165">O objeto [**DiskQuotaControl**](diskquotacontrol-object.md) exporta um método enumerador padrão que permite enumerar a coleção de objetos **DIDiskQuotaUser** .</span><span class="sxs-lookup"><span data-stu-id="30002-165">The [**DiskQuotaControl**](diskquotacontrol-object.md) object exports a standard enumerator method that allows you to enumerate the collection of **DIDiskQuotaUser** objects.</span></span> <span data-ttu-id="30002-166">O procedimento a seguir ilustra como executar a enumeração com o Microsoft JScript (compatível com a especificação de linguagem ECMA 262).</span><span class="sxs-lookup"><span data-stu-id="30002-166">The following procedure illustrates how to perform the enumeration with Microsoft JScript (compatible with ECMA 262 language specification).</span></span> <span data-ttu-id="30002-167">Você pode usar um procedimento semelhante com o Visual Basic ou o Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="30002-167">You can use a similar procedure with Visual Basic or Microsoft Visual Basic Scripting Edition (VBScript).</span></span>

1.  <span data-ttu-id="30002-168">Crie um novo [**objeto DiskQuotaControl.**](diskquotacontrol-object.md)</span><span class="sxs-lookup"><span data-stu-id="30002-168">Create a new [**DiskQuotaControl**](diskquotacontrol-object.md) object.</span></span>
2.  <span data-ttu-id="30002-169">Inicialize-o com [**Inicializar**](diskquotacontrol-initialize.md).</span><span class="sxs-lookup"><span data-stu-id="30002-169">Initialize it with [**Initialize**](diskquotacontrol-initialize.md).</span></span>
3.  <span data-ttu-id="30002-170">Crie um novo objeto **enumerador JScript.**</span><span class="sxs-lookup"><span data-stu-id="30002-170">Create a new JScript **Enumerator** object.</span></span>
4.  <span data-ttu-id="30002-171">Use um loop **for** para enumerar os **objetos DIDiskQuotaUser.**</span><span class="sxs-lookup"><span data-stu-id="30002-171">Use a **for** loop to enumerate the **DIDiskQuotaUser** objects.</span></span> <span data-ttu-id="30002-172">Não é necessário definir um valor inicial.</span><span class="sxs-lookup"><span data-stu-id="30002-172">There is no need to set a starting value.</span></span> <span data-ttu-id="30002-173">O método **moveNext** do objeto enumerador notifica o método **de item** para retornar o próximo **objeto DIDiskQuotaUser.**</span><span class="sxs-lookup"><span data-stu-id="30002-173">The enumerator object's **moveNext** method notifies the **item** method to return the next **DIDiskQuotaUser** object.</span></span> <span data-ttu-id="30002-174">O **método atEnd** retorna **false** quando você chega ao final da lista.</span><span class="sxs-lookup"><span data-stu-id="30002-174">The **atEnd** method returns **false** when you reach the end of the list.</span></span>
5.  <span data-ttu-id="30002-175">Conforme necessário, use o objeto **DIDiskQuotaUser** retornado pelo método **de item** do enumerador para recuperar ou definir uma ou mais das propriedades de cota de disco do usuário associado.</span><span class="sxs-lookup"><span data-stu-id="30002-175">As needed, use the **DIDiskQuotaUser** object returned by the enumerator's **item** method to retrieve or set one or more of the associated user's disk quota properties.</span></span>

<span data-ttu-id="30002-176">O fragmento de código a seguir ilustra como enumerar objetos **DIDiskQuotaUser** com JScript.</span><span class="sxs-lookup"><span data-stu-id="30002-176">The following code fragment illustrates how to enumerate **DIDiskQuotaUser** objects with JScript.</span></span> <span data-ttu-id="30002-177">O **argumento \_ Rótulo** de Volume passado para a **função EnumUsers** é um valor de cadeia de caracteres que contém um rótulo de volume como "C: \\ \\ ".</span><span class="sxs-lookup"><span data-stu-id="30002-177">The **Volume\_Label** argument that is passed to the **EnumUsers** function is a string value containing a volume label such as "C:\\\\".</span></span>


```
function EnumUsers(Volume_Label)
{
    var Volume;
    var QuotaUsers;
    var QuotaUser;

    Volume = new ActiveXObject("Microsoft.DiskQuota.1");
    Volume.Initialize(Volume_Label, 1);

    QuotaUsers = new Enumerator(Volume);
    for (;!Users.atEnd(); Users.moveNext())
    {
       QuotaUser = QuotaUsers.item();

     //Use the QuotaUser object to retrieve or set one or more
     //of the user's disk quota properties
     ...
    }
}
```



## <a name="requirements"></a><span data-ttu-id="30002-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30002-178">Requirements</span></span>



| <span data-ttu-id="30002-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="30002-179">Requirement</span></span> | <span data-ttu-id="30002-180">Valor</span><span class="sxs-lookup"><span data-stu-id="30002-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30002-181">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30002-181">Minimum supported client</span></span><br/> | <span data-ttu-id="30002-182">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="30002-182">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="30002-183">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30002-183">Minimum supported server</span></span><br/> | <span data-ttu-id="30002-184">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="30002-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="30002-185">DLL</span><span class="sxs-lookup"><span data-stu-id="30002-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30002-186"><dt>Shell32.dll (versão 5.0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="30002-186"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30002-187">Confira também</span><span class="sxs-lookup"><span data-stu-id="30002-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30002-188">**Objeto Shell**</span><span class="sxs-lookup"><span data-stu-id="30002-188">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 




