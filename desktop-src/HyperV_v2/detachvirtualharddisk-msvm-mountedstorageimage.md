---
description: Desanexa a imagem de armazenamento montada que está associada a essa classe.
ms.assetid: C3AB0EEE-71FE-4049-90AB-01F5D77E3B97
title: Método DetachVirtualHardDisk da classe Msvm_MountedStorageImage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MountedStorageImage.DetachVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0d411134d85fe70163b2e08eebed0ff0d4b88e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758803"
---
# <a name="detachvirtualharddisk-method-of-the-msvm_mountedstorageimage-class"></a><span data-ttu-id="bbc4f-103">Método DetachVirtualHardDisk da \_ classe MountedStorageImage Msvm</span><span class="sxs-lookup"><span data-stu-id="bbc4f-103">DetachVirtualHardDisk method of the Msvm\_MountedStorageImage class</span></span>

<span data-ttu-id="bbc4f-104">Desanexa a imagem de armazenamento montada que está associada a essa classe.</span><span class="sxs-lookup"><span data-stu-id="bbc4f-104">Detaches the mounted storage image that is associated with this class.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbc4f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbc4f-105">Syntax</span></span>


```mof
uint32 DetachVirtualHardDisk();
```



## <a name="parameters"></a><span data-ttu-id="bbc4f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbc4f-106">Parameters</span></span>

<span data-ttu-id="bbc4f-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bbc4f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bbc4f-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bbc4f-108">Return value</span></span>

<span data-ttu-id="bbc4f-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bbc4f-109">Type: **uint32**</span></span>

<span data-ttu-id="bbc4f-110">Esse método pode retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="bbc4f-110">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="bbc4f-111">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="bbc4f-111">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bbc4f-112">**Falha** (1)</span><span class="sxs-lookup"><span data-stu-id="bbc4f-112">**Failed** (1)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="bbc4f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="bbc4f-113">Remarks</span></span>

<span data-ttu-id="bbc4f-114">O acesso à classe [**Msvm \_ MountedStorageImage**](msvm-mountedstorageimage.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="bbc4f-114">Access to the [**Msvm\_MountedStorageImage**](msvm-mountedstorageimage.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="bbc4f-115">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="bbc4f-115">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="bbc4f-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bbc4f-116">Examples</span></span>

<span data-ttu-id="bbc4f-117">O exemplo de C# a seguir mostra como desanexar um arquivo de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="bbc4f-117">The following C# example shows how to detach a virtual hard disk file.</span></span> <span data-ttu-id="bbc4f-118">Os utilitários referenciados podem ser encontrados em [utilitários comuns para os exemplos de virtualização (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="bbc4f-118">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void DetachVirtualHardDisk(string path)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);

    ManagementClass mountedStorageImageServiceClass = new ManagementClass("Msvm_MountedStorageImage");

    mountedStorageImageServiceClass.Scope = scope;

    using (ManagementObjectCollection collection = mountedStorageImageServiceClass.GetInstances())
    {
        foreach (ManagementObject image in collection)
        {
            using (image)
            {
                string name = image.GetPropertyValue("Name").ToString();
                if (string.Equals(name, path, StringComparison.OrdinalIgnoreCase))
                {
                    ManagementBaseObject outParams = image.InvokeMethod("DetachVirtualHardDisk", null, null);

                    if ((UInt32)outParams["ReturnValue"] == 0)
                    {
                        Console.WriteLine("{0} was detached successfully.", path);
                    }
                    else
                    {
                        Console.WriteLine("Unable to dettach {0}", path);
                    }

                    outParams.Dispose();

                    break;
                }

                image.Dispose();
            }
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="bbc4f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbc4f-119">Requirements</span></span>



| <span data-ttu-id="bbc4f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbc4f-120">Requirement</span></span> | <span data-ttu-id="bbc4f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="bbc4f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbc4f-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bbc4f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bbc4f-123">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="bbc4f-123">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bbc4f-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bbc4f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bbc4f-125">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="bbc4f-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bbc4f-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="bbc4f-126">Namespace</span></span><br/>                | <span data-ttu-id="bbc4f-127">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="bbc4f-127">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bbc4f-128">MOF</span><span class="sxs-lookup"><span data-stu-id="bbc4f-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bbc4f-129"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bbc4f-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bbc4f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="bbc4f-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbc4f-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bbc4f-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bbc4f-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="bbc4f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbc4f-133">**Msvm \_ MountedStorageImage**</span><span class="sxs-lookup"><span data-stu-id="bbc4f-133">**Msvm\_MountedStorageImage**</span></span>](msvm-mountedstorageimage.md)
</dt> </dl>

 

