---
title: Otimização usando GetInfoEx
description: Usado para carregar valores de atributo específicos no cache local do serviço de diretório subjacente.
ms.assetid: e6111957-22cb-4473-9814-5bcbc79583b2
ms.tgt_platform: multiple
keywords:
- Otimização usando a ADSI GetInfoEx
- GetInfoEx ADSI, otimização usando IADs GetInfoEx
- ADSI ADSI, usando, otimização usando o método IADs GetInfoEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b522093fff00700cf35b864edde2a6ae7f8f9922
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294499"
---
# <a name="optimization-using-getinfoex"></a><span data-ttu-id="74f32-106">Otimização usando GetInfoEx</span><span class="sxs-lookup"><span data-stu-id="74f32-106">Optimization Using GetInfoEx</span></span>

<span data-ttu-id="74f32-107">O método [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) é usado para carregar valores de atributo específicos no cache local do serviço de diretório subjacente.</span><span class="sxs-lookup"><span data-stu-id="74f32-107">The [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method is used to load specific attribute values into the local cache from the underlying directory service.</span></span> <span data-ttu-id="74f32-108">Esse método carrega apenas os valores de atributo especificados no cache local.</span><span class="sxs-lookup"><span data-stu-id="74f32-108">This method only loads the specified attribute values into the local cache.</span></span> <span data-ttu-id="74f32-109">O método [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) é usado para carregar todos os valores de atributo no cache local.</span><span class="sxs-lookup"><span data-stu-id="74f32-109">The [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method is used to load all attribute values into the local cache.</span></span>

<span data-ttu-id="74f32-110">O método [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) obtém valores atuais específicos para as propriedades de um objeto Active Directory do repositório de diretórios subjacente, atualizando os valores armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="74f32-110">The [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method gets specific current values for the properties of an Active Directory object from the underlying directory store, refreshing the cached values.</span></span>

<span data-ttu-id="74f32-111">No entanto, se um valor já existir no cache de propriedades, chamar o método [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) ou [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) sem primeiro chamar [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) para esse atributo recuperará o valor em cache em vez do valor mais atual do diretório subjacente.</span><span class="sxs-lookup"><span data-stu-id="74f32-111">If a value already exists in the property cache, however, calling the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) or [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method without first calling [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) for that attribute will retrieve the cached value rather than the most current value from the underlying directory.</span></span> <span data-ttu-id="74f32-112">Isso pode fazer com que os valores de atributo atualizados sejam substituídos se o cache local tiver sido modificado, mas os valores não tiverem sido confirmados no serviço de diretório subjacente com uma chamada para o método [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="74f32-112">This can cause updated attribute values to be overwritten if the local cache has been modified, but the values have not been committed to the underlying directory service with a call to the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method.</span></span> <span data-ttu-id="74f32-113">O método sugerido para evitar problemas de cache é sempre confirmar alterações de valor de atributo chamando **IADs. setinfo** antes de chamar [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo).</span><span class="sxs-lookup"><span data-stu-id="74f32-113">The suggested method for avoiding caching problems is to always commit attribute value changes by calling **IADs.SetInfo** before calling [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo).</span></span>


```VB
Dim usr As IADs
Dim PropArray As Variant

On Error GoTo Cleanup

' Bind to a specific user object.
Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' The code example assumes that the property description has a single value in the directory.
' Be aware that this will implicitly call GetInfo because, at this point, GetInfo
' has not yet been called (implicitly or explicitly) on the usr object.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Change two of the attribute values in the local cache.
usr.Put "cn", "Jeff Smith"
usr.Put "title", "Vice President"
usr.Put "department", "Head Office"
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Initialize the array of properties to pass to GetInfoEx.
PropArray = Array("department", "title")
 
' Get the specified attribute values.
usr.GetInfoEx PropArray, 0

' The specific attributes values were overwritten, but the attribute
' value not retrieved has not changed.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



## <a name="retrieving-active-directory-constructed-attributes"></a><span data-ttu-id="74f32-114">Recuperando Active Directory atributos construídos</span><span class="sxs-lookup"><span data-stu-id="74f32-114">Retrieving Active Directory Constructed Attributes</span></span>

<span data-ttu-id="74f32-115">Em Active Directory, a maioria dos atributos construídos é recuperada e armazenada em cache quando o método [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) é chamado ([**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) executa uma chamada de **IADs. GetInfo** implícita se o cache estiver vazio).</span><span class="sxs-lookup"><span data-stu-id="74f32-115">In Active Directory, most of the constructed attributes are retrieved and cached when the [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method is called ([**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) performs an implicit **IADs.GetInfo** call if the cache is empty).</span></span> <span data-ttu-id="74f32-116">Alguns atributos construídos, no entanto, não são automaticamente recuperados e armazenados em cache e, portanto, exigem que o método [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) seja chamado explicitamente para recuperá-los.</span><span class="sxs-lookup"><span data-stu-id="74f32-116">Some constructed attributes, however, are not automatically retrieved and cached and, therefore, require that the [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method be called explicitly to retrieve them.</span></span> <span data-ttu-id="74f32-117">Por exemplo, em Active Directory, o atributo [**canôniconame**](/windows/desktop/ADSchema/a-canonicalname) não é recuperado quando o método **IADs. GetInfo** é chamado e **IADs. Get** retornará a **\_ propriedade e ADS \_ \_ não \_ encontrada**.</span><span class="sxs-lookup"><span data-stu-id="74f32-117">For example, in Active Directory, the [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname) attribute is not retrieved when the **IADs.GetInfo** method is called and **IADs.Get** will return **E\_ADS\_PROPERTY\_NOT\_FOUND**.</span></span> <span data-ttu-id="74f32-118">O método **IADs. GetInfoEx** deve ser chamado para recuperar o atributo **canôniconame** .</span><span class="sxs-lookup"><span data-stu-id="74f32-118">The **IADs.GetInfoEx** method must be called to retrieve the **canonicalName** attribute.</span></span> <span data-ttu-id="74f32-119">Esses mesmos atributos construídos também não serão recuperados usando a interface [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) para enumerar os atributos.</span><span class="sxs-lookup"><span data-stu-id="74f32-119">These same constructed attributes will also not be retrieved using the [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) interface to enumerate the attributes.</span></span>

<span data-ttu-id="74f32-120">Para obter mais informações e um exemplo de código que mostra como recuperar todos os valores de atributo, consulte [exemplo de código para ler um atributo construído](example-code-for-reading-a-constructed-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="74f32-120">For more information and a code example that shows how to retrieve all attribute values, see [Example Code for Reading a Constructed Attribute](example-code-for-reading-a-constructed-attribute.md).</span></span>

 

 