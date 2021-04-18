---
description: A Propriedade ColumnInfo do objeto View retorna um objeto Record contendo as informações solicitadas sobre cada coluna no conjunto de resultados.
ms.assetid: 8cfa504c-a6f1-443e-9b3a-b230c4c39b64
title: Propriedade View. ColumnInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.ColumnInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 38c016b15108446cc04114adc06ad12686d9932c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752236"
---
# <a name="viewcolumninfo-property"></a><span data-ttu-id="2c891-103">Propriedade View. ColumnInfo</span><span class="sxs-lookup"><span data-stu-id="2c891-103">View.ColumnInfo property</span></span>

<span data-ttu-id="2c891-104">A propriedade **ColumnInfo** do objeto [**View**](view-object.md) retorna um objeto [**Record**](record-object.md) contendo as informações solicitadas sobre cada coluna no conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="2c891-104">The **ColumnInfo** property of the [**View**](view-object.md) object returns a [**Record**](record-object.md) object containing the requested information about each column in the result set.</span></span> <span data-ttu-id="2c891-105">Os nomes de coluna ou as definições de coluna podem ser solicitadas.</span><span class="sxs-lookup"><span data-stu-id="2c891-105">Either the column names or the column definitions may be requested.</span></span> <span data-ttu-id="2c891-106">As constantes fornecidas na lista de seleção não têm nomes.</span><span class="sxs-lookup"><span data-stu-id="2c891-106">Constants supplied in the Select list do not have names.</span></span>

<span data-ttu-id="2c891-107">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="2c891-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c891-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c891-108">Syntax</span></span>


```JScript
propVal = View.ColumnInfo
```



## <a name="property-value"></a><span data-ttu-id="2c891-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2c891-109">Property value</span></span>

<span data-ttu-id="2c891-110">Informações obrigatórias necessárias para cada coluna.</span><span class="sxs-lookup"><span data-stu-id="2c891-110">Required information needed for each column.</span></span>



| <span data-ttu-id="2c891-111">Nome do parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c891-111">Parameter name</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="2c891-112">Significado</span><span class="sxs-lookup"><span data-stu-id="2c891-112">Meaning</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="msiColumnInfoNames"></span><span id="msicolumninfonames"></span><span id="MSICOLUMNINFONAMES"></span><dl> <span data-ttu-id="2c891-113"><dt>**msiColumnInfoNames**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2c891-113"><dt>**msiColumnInfoNames**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="2c891-114">Retorna os nomes de todas as colunas não constantes no conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="2c891-114">Returns the names of all nonconstant columns in result set.</span></span><br/> |
| <span id="msiColumnInfoTypes"></span><span id="msicolumninfotypes"></span><span id="MSICOLUMNINFOTYPES"></span><dl> <span data-ttu-id="2c891-115"><dt>**msiColumnInfoTypes**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2c891-115"><dt>**msiColumnInfoTypes**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="2c891-116">Retorna os tipos de todas as colunas não constantes no conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="2c891-116">Returns the types of all nonconstant columns in result set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2c891-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c891-117">Remarks</span></span>

<span data-ttu-id="2c891-118">As descrições de coluna retornadas pela propriedade **ColumnInfo** estão no formato descrito em [formato de definição de coluna](column-definition-format.md).</span><span class="sxs-lookup"><span data-stu-id="2c891-118">The column descriptions returned by the **ColumnInfo** property are in the format described in [Column Definition Format](column-definition-format.md).</span></span> <span data-ttu-id="2c891-119">Cada coluna é descrita por uma cadeia de caracteres no campo registro correspondente.</span><span class="sxs-lookup"><span data-stu-id="2c891-119">Each column is described by a string in the corresponding record field.</span></span> <span data-ttu-id="2c891-120">A cadeia de caracteres de definição consiste em uma única letra que representa o tipo de dados seguido pela largura da coluna (em caracteres quando aplicável, ou outros bytes).</span><span class="sxs-lookup"><span data-stu-id="2c891-120">The definition string consists of a single letter representing the data type followed by the width of the column (in characters when applicable, or else bytes).</span></span> <span data-ttu-id="2c891-121">Uma largura de zero designa uma largura não associada (fluxos e campos de texto longos).</span><span class="sxs-lookup"><span data-stu-id="2c891-121">A width of zero designates an unbounded width (long text fields and streams).</span></span> <span data-ttu-id="2c891-122">Uma letra maiúscula indica que valores nulos são permitidos na coluna.</span><span class="sxs-lookup"><span data-stu-id="2c891-122">An uppercase letter indicates that Null values are allowed in the column.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c891-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c891-123">Requirements</span></span>



| <span data-ttu-id="2c891-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c891-124">Requirement</span></span> | <span data-ttu-id="2c891-125">Valor</span><span class="sxs-lookup"><span data-stu-id="2c891-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c891-126">Versão</span><span class="sxs-lookup"><span data-stu-id="2c891-126">Version</span></span><br/> | <span data-ttu-id="2c891-127">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2c891-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2c891-128">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2c891-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2c891-129">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="2c891-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="2c891-130">DLL</span><span class="sxs-lookup"><span data-stu-id="2c891-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="2c891-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c891-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="2c891-132">IID</span><span class="sxs-lookup"><span data-stu-id="2c891-132">IID</span></span><br/>     | <span data-ttu-id="2c891-133">IID \_ IView é definido como 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2c891-133">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




