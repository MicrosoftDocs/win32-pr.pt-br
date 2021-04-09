---
description: A \_ classe de montagem CIM representa uma associação entre um sistema de arquivos e um diretório ao qual ele está anexado.
ms.assetid: abf1833b-9b39-45c0-8400-2be2bf3a1c3c
ms.tgt_platform: multiple
title: Classe CIM_Mount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Mount
- CIM_Mount.Dependent
- CIM_Mount.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5b86587466517a10302b3109a521e902a66892c4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089336"
---
# <a name="cim_mount-class"></a><span data-ttu-id="05df1-103">\_Classe de montagem CIM</span><span class="sxs-lookup"><span data-stu-id="05df1-103">CIM\_Mount class</span></span>

<span data-ttu-id="05df1-104">A classe de **\_ montagem CIM** representa uma associação entre um sistema de arquivos e um diretório ao qual ele está anexado.</span><span class="sxs-lookup"><span data-stu-id="05df1-104">The **CIM\_Mount** class represents an association between a file system and a directory to which it is attached.</span></span>

<span data-ttu-id="05df1-105">A semântica dessa relação exige que o diretório montado seja contido por um sistema de arquivos (por meio da Associação de armazenamento de arquivo) que seja diferente do sistema de arquivos referenciado como dependente.</span><span class="sxs-lookup"><span data-stu-id="05df1-105">The semantics of this relationship require that the mounted directory be contained by a file system (via the file storage association) that is different from the file system referenced as the dependent.</span></span> <span data-ttu-id="05df1-106">O sistema de arquivos que contém o diretório pode ser local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="05df1-106">The directory's containing file system can be local or remote.</span></span> <span data-ttu-id="05df1-107">Por exemplo, um sistema de arquivos local em um sistema de computador Solaris pode montar um diretório do sistema de arquivos acessado por meio da unidade de CDROM do computador (ou seja, outro sistema de arquivos local).</span><span class="sxs-lookup"><span data-stu-id="05df1-107">For example, a local file system on a Solaris computer system can mount a directory from the file system accessed via the computer's CDROM drive (that is, another local file system).</span></span> <span data-ttu-id="05df1-108">Por outro lado, em um caso "remoto", o diretório é primeiro exportado por seu sistema de arquivos, que é hospedado em outro sistema de computador agindo, por exemplo, como um servidor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="05df1-108">On the other hand, in a "remote" case, the directory is first exported by its file system, which is hosted on another computer system acting, for example, as a file server.</span></span> <span data-ttu-id="05df1-109">Para distinguir as duas montagens, uma associação [**de \_ exportação de CIM**](cim-export.md) sempre deve ser definida para os diretórios acessados/montados remotamente.</span><span class="sxs-lookup"><span data-stu-id="05df1-109">To distinguish the two mounts, a [**CIM\_Export**](cim-export.md) association should always be defined for the remotely accessed/mounted directories.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="05df1-110">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="05df1-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="05df1-111">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="05df1-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="05df1-112">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="05df1-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="05df1-113">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="05df1-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="05df1-114">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05df1-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4F6-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_Mount : CIM_Dependency
{
  CIM_NFS       REF Dependent;
  CIM_Directory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="05df1-115">Membros</span><span class="sxs-lookup"><span data-stu-id="05df1-115">Members</span></span>

<span data-ttu-id="05df1-116">A classe de **\_ montagem CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="05df1-116">The **CIM\_Mount** class has these types of members:</span></span>

-   [<span data-ttu-id="05df1-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="05df1-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="05df1-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="05df1-118">Properties</span></span>

<span data-ttu-id="05df1-119">A classe de **\_ montagem CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="05df1-119">The **CIM\_Mount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="05df1-120">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="05df1-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05df1-121">Tipo de dados **: \_ diretório CIM**</span><span class="sxs-lookup"><span data-stu-id="05df1-121">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="05df1-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="05df1-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05df1-123">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="05df1-123">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="05df1-124">Um [**\_ diretório CIM**](cim-directory.md) que descreve o diretório montado.</span><span class="sxs-lookup"><span data-stu-id="05df1-124">A [**CIM\_Directory**](cim-directory.md) describing the directory mounted.</span></span>

</dd> <dt>

<span data-ttu-id="05df1-125">**Depende**</span><span class="sxs-lookup"><span data-stu-id="05df1-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05df1-126">Tipo de dados: **CIM \_ NFS**</span><span class="sxs-lookup"><span data-stu-id="05df1-126">Data type: **CIM\_NFS**</span></span>
</dt> <dt>

<span data-ttu-id="05df1-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="05df1-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05df1-128">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="05df1-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="05df1-129">Um [**\_ NFS do CIM**](cim-nfs.md) que descreve o sistema de arquivos no qual o diretório está montado.</span><span class="sxs-lookup"><span data-stu-id="05df1-129">A [**CIM\_NFS**](cim-nfs.md) describing the FileSystem the Directory is mounted on.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05df1-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="05df1-130">Remarks</span></span>

<span data-ttu-id="05df1-131">**CIM \_ A montagem** é derivada [**da \_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="05df1-131">**CIM\_Mount** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="05df1-132">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="05df1-132">WMI does not implement this class.</span></span>

<span data-ttu-id="05df1-133">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="05df1-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="05df1-134">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="05df1-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="05df1-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05df1-135">Requirements</span></span>



| <span data-ttu-id="05df1-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="05df1-136">Requirement</span></span> | <span data-ttu-id="05df1-137">Valor</span><span class="sxs-lookup"><span data-stu-id="05df1-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05df1-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05df1-138">Minimum supported client</span></span><br/> | <span data-ttu-id="05df1-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="05df1-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="05df1-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05df1-140">Minimum supported server</span></span><br/> | <span data-ttu-id="05df1-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05df1-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="05df1-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="05df1-142">Namespace</span></span><br/>                | <span data-ttu-id="05df1-143">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="05df1-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="05df1-144">MOF</span><span class="sxs-lookup"><span data-stu-id="05df1-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05df1-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="05df1-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="05df1-146">DLL</span><span class="sxs-lookup"><span data-stu-id="05df1-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05df1-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05df1-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05df1-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="05df1-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05df1-149">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="05df1-149">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

