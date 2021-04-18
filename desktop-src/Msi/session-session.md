---
description: A Propriedade Property do objeto Session é uma propriedade de leitura/gravação que representa o valor da cadeia de caracteres de uma propriedade nomeada do instalador, conforme mantida pelo objeto Session.
ms.assetid: 15ce8264-2573-428c-98d9-690cfaae5144
title: Propriedade Session. Property
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9635d5b9ee093f270e4ee7993f78609d60caa13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792483"
---
# <a name="sessionproperty-property"></a><span data-ttu-id="1a184-103">Propriedade Session. Property</span><span class="sxs-lookup"><span data-stu-id="1a184-103">Session.Property property</span></span>

<span data-ttu-id="1a184-104">A propriedade **Property** do objeto [**Session**](session-object.md) é uma propriedade de leitura/gravação que representa o valor da cadeia de caracteres de uma propriedade nomeada do instalador, conforme mantida pelo objeto de **sessão** na tabela de propriedades na memória, ou, se for prefixada com um sinal de porcentagem (%), o valor de uma variável de ambiente do sistema para o processo atual.</span><span class="sxs-lookup"><span data-stu-id="1a184-104">The **Property** property of the [**Session**](session-object.md) object is a read-write property that represents the string value of a named installer property, as maintained by the **Session** object in the in-memory Property table, or, if it is prefixed with a percent sign (%), the value of a system environment variable for the current process.</span></span> <span data-ttu-id="1a184-105">Os valores de cadeia de caracteres ou inteiros podem ser fornecidos.</span><span class="sxs-lookup"><span data-stu-id="1a184-105">Either string or integer values may be supplied.</span></span> <span data-ttu-id="1a184-106">Uma propriedade ou variável de ambiente não existente é equivalente ao valor que está sendo nulo.</span><span class="sxs-lookup"><span data-stu-id="1a184-106">A non-existent property or environment variable is equivalent to its value being Null.</span></span>

<span data-ttu-id="1a184-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1a184-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a184-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a184-108">Syntax</span></span>


```JScript
propVal = Session.Property
Session.Property = propVal 
```



## <a name="property-value"></a><span data-ttu-id="1a184-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1a184-109">Property value</span></span>

<span data-ttu-id="1a184-110">O nome de uma propriedade que diferencia maiúsculas de minúsculas ou um nome que não diferencia maiúsculas de minúsculas de uma variável de ambiente prefixado por um sinal de porcentagem (%).</span><span class="sxs-lookup"><span data-stu-id="1a184-110">Required case-sensitive name of a property, or a case-insensitive name of an environment variable prefixed by a percent sign (%).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a184-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a184-111">Requirements</span></span>



| <span data-ttu-id="1a184-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a184-112">Requirement</span></span> | <span data-ttu-id="1a184-113">Valor</span><span class="sxs-lookup"><span data-stu-id="1a184-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a184-114">Versão</span><span class="sxs-lookup"><span data-stu-id="1a184-114">Version</span></span><br/> | <span data-ttu-id="1a184-115">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1a184-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1a184-116">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1a184-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1a184-117">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="1a184-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="1a184-118">DLL</span><span class="sxs-lookup"><span data-stu-id="1a184-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="1a184-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a184-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="1a184-120">IID</span><span class="sxs-lookup"><span data-stu-id="1a184-120">IID</span></span><br/>     | <span data-ttu-id="1a184-121">IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="1a184-121">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




