---
description: O método ReadStream do objeto de registro lê um número especificado de bytes de um campo de registro que contém dados de fluxo.
ms.assetid: 845e23e5-6379-4592-aee4-cd6832baf335
title: Método record. ReadStream
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.ReadStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: bc77e07231d086f15086662d60581d4c5992bf5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758950"
---
# <a name="recordreadstream-method"></a><span data-ttu-id="76ec5-103">Método record. ReadStream</span><span class="sxs-lookup"><span data-stu-id="76ec5-103">Record.ReadStream method</span></span>

<span data-ttu-id="76ec5-104">O método **ReadStream** do objeto de [**registro**](record-object.md) lê um número especificado de bytes de um campo de registro que contém dados de fluxo.</span><span class="sxs-lookup"><span data-stu-id="76ec5-104">The **ReadStream** method of the [**Record**](record-object.md) object reads a specified number of bytes from a record field that contains stream data.</span></span>

## <a name="syntax"></a><span data-ttu-id="76ec5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76ec5-105">Syntax</span></span>


```JScript
Record.ReadStream(
  field,
  length,
  format
)
```



## <a name="parameters"></a><span data-ttu-id="76ec5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76ec5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76ec5-107">*campo*</span><span class="sxs-lookup"><span data-stu-id="76ec5-107">*field*</span></span> 
</dt> <dd>

<span data-ttu-id="76ec5-108">O número de campo necessário do valor dentro do registro, baseado em 1.</span><span class="sxs-lookup"><span data-stu-id="76ec5-108">The required field number of the value within the record, 1-based.</span></span>

</dd> <dt>

<span data-ttu-id="76ec5-109">*length*</span><span class="sxs-lookup"><span data-stu-id="76ec5-109">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="76ec5-110">O número necessário de bytes para ler a partir do fluxo.</span><span class="sxs-lookup"><span data-stu-id="76ec5-110">The required number of bytes to read from the stream.</span></span>

</dd> <dt>

<span data-ttu-id="76ec5-111">*format*</span><span class="sxs-lookup"><span data-stu-id="76ec5-111">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="76ec5-112">Interpretação necessária e retorno dos bytes de dados.</span><span class="sxs-lookup"><span data-stu-id="76ec5-112">Required interpretation and return of the data bytes.</span></span>



| <span data-ttu-id="76ec5-113">Nome do parâmetro</span><span class="sxs-lookup"><span data-stu-id="76ec5-113">Parameter name</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="76ec5-114">Significado</span><span class="sxs-lookup"><span data-stu-id="76ec5-114">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="msiReadStreamInteger"></span><span id="msireadstreaminteger"></span><span id="MSIREADSTREAMINTEGER"></span><dl> <span data-ttu-id="76ec5-115"><dt>**msiReadStreamInteger**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="76ec5-115"><dt>**msiReadStreamInteger**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="76ec5-116">Como um inteiro longo, o comprimento deve ser de 1 a 4.</span><span class="sxs-lookup"><span data-stu-id="76ec5-116">As a long integer the length must be 1 to 4.</span></span><br/>             |
| <span id="msiReadStreamBytes"></span><span id="msireadstreambytes"></span><span id="MSIREADSTREAMBYTES"></span><dl> <span data-ttu-id="76ec5-117"><dt>**msiReadStreamBytes**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="76ec5-117"><dt>**msiReadStreamBytes**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="76ec5-118">Os dados como um **BSTR**– um byte por caractere.</span><span class="sxs-lookup"><span data-stu-id="76ec5-118">The data as a **BSTR**—one byte per character.</span></span><br/>           |
| <span id="msiReadStreamAnsi"></span><span id="msireadstreamansi"></span><span id="MSIREADSTREAMANSI"></span><dl> <span data-ttu-id="76ec5-119"><dt>**msiReadStreamAnsi**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="76ec5-119"><dt>**msiReadStreamAnsi**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="76ec5-120">Os bytes ANSI convertidos em um **BSTR** Unicode.</span><span class="sxs-lookup"><span data-stu-id="76ec5-120">The ANSI bytes translated to a Unicode **BSTR**.</span></span><br/>         |
| <span id="msiReadStreamDirect"></span><span id="msireadstreamdirect"></span><span id="MSIREADSTREAMDIRECT"></span><dl> <span data-ttu-id="76ec5-121"><dt>**msiReadStreamDirect**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="76ec5-121"><dt>**msiReadStreamDirect**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="76ec5-122">Os pares de bytes retornados diretamente como um **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="76ec5-122">The byte pairs that are returned directly as a **BSTR**.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76ec5-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="76ec5-123">Return value</span></span>

<span data-ttu-id="76ec5-124">Esse método retorna uma cadeia de caracteres que contém o número solicitado de bytes lidos de um campo de registro.</span><span class="sxs-lookup"><span data-stu-id="76ec5-124">This method returns a string that contains the requested number of bytes read from a record field.</span></span>

## <a name="remarks"></a><span data-ttu-id="76ec5-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="76ec5-125">Remarks</span></span>

<span data-ttu-id="76ec5-126">O valor retornado de um campo inexistente é um valor vazio.</span><span class="sxs-lookup"><span data-stu-id="76ec5-126">The returned value of a nonexistent field is an Empty value.</span></span> <span data-ttu-id="76ec5-127">Se o fluxo tiver menos bytes que a contagem solicitada, a cadeia de caracteres retornada será reduzida adequadamente.</span><span class="sxs-lookup"><span data-stu-id="76ec5-127">If the stream has fewer bytes that the count requested, the returned string is shortened appropriately.</span></span>

<span data-ttu-id="76ec5-128">Para obter um exemplo desse método, consulte [Copiar arquivo ANSI em um campo de banco de dados](copy-ansi-file-into-a-database-field.md).</span><span class="sxs-lookup"><span data-stu-id="76ec5-128">For an example of this method, see [Copy ANSI File Into a Database Field](copy-ansi-file-into-a-database-field.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="76ec5-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76ec5-129">Requirements</span></span>



| <span data-ttu-id="76ec5-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="76ec5-130">Requirement</span></span> | <span data-ttu-id="76ec5-131">Valor</span><span class="sxs-lookup"><span data-stu-id="76ec5-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76ec5-132">Versão</span><span class="sxs-lookup"><span data-stu-id="76ec5-132">Version</span></span><br/> | <span data-ttu-id="76ec5-133">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="76ec5-133">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="76ec5-134">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="76ec5-134">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="76ec5-135">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="76ec5-135">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="76ec5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="76ec5-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="76ec5-137"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76ec5-137"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="76ec5-138">IID</span><span class="sxs-lookup"><span data-stu-id="76ec5-138">IID</span></span><br/>     | <span data-ttu-id="76ec5-139">IID \_ IRecord é definido como 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="76ec5-139">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




