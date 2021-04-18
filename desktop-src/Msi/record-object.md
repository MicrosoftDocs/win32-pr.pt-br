---
description: O objeto Record é um contêiner para manter e transferir um número variável de valores.
ms.assetid: e832c19f-61a6-4e42-a10a-b7bb1705af59
title: Objeto de registro
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c13cb31d628525e529491af1c089555ba2ad8273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751634"
---
# <a name="record-object"></a><span data-ttu-id="f71ed-103">Objeto de registro</span><span class="sxs-lookup"><span data-stu-id="f71ed-103">Record object</span></span>

<span data-ttu-id="f71ed-104">O objeto **Record** é um contêiner para manter e transferir um número variável de valores.</span><span class="sxs-lookup"><span data-stu-id="f71ed-104">The **Record** object is a container for holding and transferring a variable number of values.</span></span> <span data-ttu-id="f71ed-105">Os campos dentro do registro são indexados numericamente e podem conter cadeias de caracteres, inteiros, objetos e valores nulos.</span><span class="sxs-lookup"><span data-stu-id="f71ed-105">Fields within the record are numerically indexed and can contain strings, integers, objects, and null values.</span></span> <span data-ttu-id="f71ed-106">Os campos além do tamanho do registro alocado são tratados como tendo valores nulos permanentemente.</span><span class="sxs-lookup"><span data-stu-id="f71ed-106">Fields beyond the allocated record size are treated as having permanently null values.</span></span> <span data-ttu-id="f71ed-107">O campo número 0 está reservado.</span><span class="sxs-lookup"><span data-stu-id="f71ed-107">Field number 0 is reserved.</span></span>

## <a name="members"></a><span data-ttu-id="f71ed-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f71ed-108">Members</span></span>

<span data-ttu-id="f71ed-109">O objeto **Record** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f71ed-109">The **Record** object has these types of members:</span></span>

-   [<span data-ttu-id="f71ed-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="f71ed-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="f71ed-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f71ed-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f71ed-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="f71ed-112">Methods</span></span>

<span data-ttu-id="f71ed-113">O objeto **Record** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f71ed-113">The **Record** object has these methods.</span></span>



| <span data-ttu-id="f71ed-114">Método</span><span class="sxs-lookup"><span data-stu-id="f71ed-114">Method</span></span>                                  | <span data-ttu-id="f71ed-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="f71ed-115">Description</span></span>                                                                                          |
|:----------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f71ed-116">**ClearData**</span><span class="sxs-lookup"><span data-stu-id="f71ed-116">**ClearData**</span></span>](record-cleardata.md)   | <span data-ttu-id="f71ed-117">Limpa os dados em todos os campos, definindo-os como NULL.</span><span class="sxs-lookup"><span data-stu-id="f71ed-117">Clears the data in all fields, setting them to null.</span></span><br/>                                      |
| [<span data-ttu-id="f71ed-118">**FormatText**</span><span class="sxs-lookup"><span data-stu-id="f71ed-118">**FormatText**</span></span>](record-formattext.md) | <span data-ttu-id="f71ed-119">Formata os campos de acordo com o modelo no campo 0.</span><span class="sxs-lookup"><span data-stu-id="f71ed-119">Formats fields according to the template in field 0.</span></span><br/>                                      |
| [<span data-ttu-id="f71ed-120">**ReadStream**</span><span class="sxs-lookup"><span data-stu-id="f71ed-120">**ReadStream**</span></span>](record-readstream.md) | <span data-ttu-id="f71ed-121">Lê um número especificado de bytes de um campo de registro que contém dados de fluxo.</span><span class="sxs-lookup"><span data-stu-id="f71ed-121">Reads a specified number of bytes from a record field holding stream data.</span></span><br/>                |
| [<span data-ttu-id="f71ed-122">**SetStream**</span><span class="sxs-lookup"><span data-stu-id="f71ed-122">**SetStream**</span></span>](record-setstream.md)   | <span data-ttu-id="f71ed-123">Copia o conteúdo do arquivo especificado para o campo registro designado como dados de fluxo.</span><span class="sxs-lookup"><span data-stu-id="f71ed-123">Copies the content of the specified file into the designated record field as stream data.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f71ed-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f71ed-124">Properties</span></span>

<span data-ttu-id="f71ed-125">O objeto **Record** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f71ed-125">The **Record** object has these properties.</span></span>



| <span data-ttu-id="f71ed-126">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f71ed-126">Property</span></span>                                             | <span data-ttu-id="f71ed-127">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="f71ed-127">Access type</span></span>           | <span data-ttu-id="f71ed-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="f71ed-128">Description</span></span>                                                                                   |
|:-----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f71ed-129">**DataSize**</span><span class="sxs-lookup"><span data-stu-id="f71ed-129">**DataSize**</span></span>](record-datasize.md)<br/>       |                       | <span data-ttu-id="f71ed-130">Retorna o tamanho dos dados para o campo designado.</span><span class="sxs-lookup"><span data-stu-id="f71ed-130">Returns the size of the data for the designated field.</span></span><br/>                             |
| [<span data-ttu-id="f71ed-131">**FieldCount**</span><span class="sxs-lookup"><span data-stu-id="f71ed-131">**FieldCount**</span></span>](record-fieldcount.md)<br/>   |                       | <span data-ttu-id="f71ed-132">Obtém o número de campos no registro.</span><span class="sxs-lookup"><span data-stu-id="f71ed-132">Returns the number of fields in the record.</span></span><br/>                                        |
| [<span data-ttu-id="f71ed-133">**IntegerData**</span><span class="sxs-lookup"><span data-stu-id="f71ed-133">**IntegerData**</span></span>](record-integerdata.md)<br/> | <span data-ttu-id="f71ed-134">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f71ed-134">Read/write</span></span><br/> | <span data-ttu-id="f71ed-135">Transfere dados inteiros de 32 bits para ou para fora de um campo especificado dentro do registro.</span><span class="sxs-lookup"><span data-stu-id="f71ed-135">Transfers 32-bit integer data in to or out of a specified field within the record.</span></span><br/> |
| [<span data-ttu-id="f71ed-136">**Énulo**</span><span class="sxs-lookup"><span data-stu-id="f71ed-136">**IsNull**</span></span>](record-isnull.md)<br/>           |                       | <span data-ttu-id="f71ed-137">Retornará true se o campo indicado for nulo e false se o campo contiver dados.</span><span class="sxs-lookup"><span data-stu-id="f71ed-137">Returns True if the indicated field is null and False if the field contains data.</span></span><br/>  |
| [<span data-ttu-id="f71ed-138">**StringData**</span><span class="sxs-lookup"><span data-stu-id="f71ed-138">**StringData**</span></span>](record-stringdata.md)<br/>   | <span data-ttu-id="f71ed-139">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f71ed-139">Read/write</span></span><br/> | <span data-ttu-id="f71ed-140">Transfere dados de cadeia de caracteres para ou para fora de um campo especificado dentro do registro.</span><span class="sxs-lookup"><span data-stu-id="f71ed-140">Transfers string data in to or out of a specified field within the record.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="f71ed-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f71ed-141">Requirements</span></span>



| <span data-ttu-id="f71ed-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="f71ed-142">Requirement</span></span> | <span data-ttu-id="f71ed-143">Valor</span><span class="sxs-lookup"><span data-stu-id="f71ed-143">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71ed-144">Versão</span><span class="sxs-lookup"><span data-stu-id="f71ed-144">Version</span></span><br/> | <span data-ttu-id="f71ed-145">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f71ed-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f71ed-146">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f71ed-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f71ed-147">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="f71ed-147">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="f71ed-148">DLL</span><span class="sxs-lookup"><span data-stu-id="f71ed-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="f71ed-149"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f71ed-149"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="f71ed-150">IID</span><span class="sxs-lookup"><span data-stu-id="f71ed-150">IID</span></span><br/>     | <span data-ttu-id="f71ed-151">IID \_ IRecord é definido como 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f71ed-151">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="f71ed-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="f71ed-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f71ed-153">**Método CreateRecord**</span><span class="sxs-lookup"><span data-stu-id="f71ed-153">**CreateRecord Method**</span></span>](installer-createrecord.md)
</dt> <dt>

[<span data-ttu-id="f71ed-154">Exemplos de script de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="f71ed-154">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




