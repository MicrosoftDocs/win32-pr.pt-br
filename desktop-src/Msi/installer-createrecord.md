---
description: O método CreateRecord do objeto instalador retorna um novo objeto de registro com o número de campos solicitado.
ms.assetid: 7f9adb28-87da-48dd-ab5c-e138b356b133
title: Método Installer. CreateRecord
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8095e35a7e424a50448f1f0d948b9224bcdaa423
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752038"
---
# <a name="installercreaterecord-method"></a><span data-ttu-id="c8c53-103">Método Installer. CreateRecord</span><span class="sxs-lookup"><span data-stu-id="c8c53-103">Installer.CreateRecord method</span></span>

<span data-ttu-id="c8c53-104">O método **CreateRecord** do objeto [**instalador**](installer-object.md) retorna um novo objeto de [**registro**](record-object.md) com o número de campos solicitado.</span><span class="sxs-lookup"><span data-stu-id="c8c53-104">The **CreateRecord** method of the [**Installer**](installer-object.md) object returns a new [**Record**](record-object.md) object with the requested number of fields.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8c53-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8c53-105">Syntax</span></span>


```JScript
Installer.CreateRecord(
  count
)
```



## <a name="parameters"></a><span data-ttu-id="c8c53-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8c53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8c53-107">*contagem*</span><span class="sxs-lookup"><span data-stu-id="c8c53-107">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="c8c53-108">Número necessário de campos, que pode ser 0.</span><span class="sxs-lookup"><span data-stu-id="c8c53-108">Required number of fields, which may be 0.</span></span> <span data-ttu-id="c8c53-109">O número máximo de campos em um registro é limitado a 65535.</span><span class="sxs-lookup"><span data-stu-id="c8c53-109">The maximum number of fields in a record is limited to 65535.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8c53-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c8c53-110">Return value</span></span>

<span data-ttu-id="c8c53-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c8c53-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8c53-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8c53-112">Remarks</span></span>

<span data-ttu-id="c8c53-113">O campo 0, não um dos campos em *contagem*, normalmente é usado para itens orientados a registros, como cadeias de caracteres de formato ou códigos op de execução.</span><span class="sxs-lookup"><span data-stu-id="c8c53-113">Field 0, not one of the fields in *count*, is normally used for record-oriented items such as format strings or execution op-codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8c53-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8c53-114">Requirements</span></span>



| <span data-ttu-id="c8c53-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8c53-115">Requirement</span></span> | <span data-ttu-id="c8c53-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c8c53-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8c53-117">Versão</span><span class="sxs-lookup"><span data-stu-id="c8c53-117">Version</span></span><br/> | <span data-ttu-id="c8c53-118">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c8c53-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c8c53-119">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c8c53-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c8c53-120">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="c8c53-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c8c53-121">DLL</span><span class="sxs-lookup"><span data-stu-id="c8c53-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="c8c53-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8c53-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c8c53-123">IID</span><span class="sxs-lookup"><span data-stu-id="c8c53-123">IID</span></span><br/>     | <span data-ttu-id="c8c53-124">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c8c53-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




