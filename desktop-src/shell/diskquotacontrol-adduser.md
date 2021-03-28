---
description: Atribui uma cota de disco não padrão a um novo usuário.
title: Método DiskQuotaControl. adduser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.AddUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: de20d016-83da-42ac-962f-86faf9b25419
ms.openlocfilehash: e91bfee0cf491d7191d64bdec6ed7593e10654ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501417"
---
# <a name="diskquotacontroladduser-method"></a><span data-ttu-id="7d320-103">Método DiskQuotaControl. adduser</span><span class="sxs-lookup"><span data-stu-id="7d320-103">DiskQuotaControl.AddUser method</span></span>

<span data-ttu-id="7d320-104">Atribui uma cota de disco não padrão a um novo usuário.</span><span class="sxs-lookup"><span data-stu-id="7d320-104">Assigns a nondefault disk quota to a new user.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d320-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7d320-105">Syntax</span></span>


```JScript
objRetVal = DiskQuotaControl.AddUser(
  sLogonName
)
```



## <a name="parameters"></a><span data-ttu-id="7d320-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d320-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d320-107">*sLogonName*</span><span class="sxs-lookup"><span data-stu-id="7d320-107">*sLogonName*</span></span> 
</dt> <dd>

<span data-ttu-id="7d320-108">Tipo: **Char**</span><span class="sxs-lookup"><span data-stu-id="7d320-108">Type: **CHAR**</span></span>

<span data-ttu-id="7d320-109">Um valor de cadeia de caracteres que contém o nome de logon do usuário.</span><span class="sxs-lookup"><span data-stu-id="7d320-109">A string value that contains the user's logon name.</span></span> <span data-ttu-id="7d320-110">Use a propriedade [**UserNameResolution**](diskquotacontrol-usernameresolution.md) para especificar como o nome deve ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="7d320-110">Use the [**UserNameResolution**](diskquotacontrol-usernameresolution.md) property to specify how the name is to be resolved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d320-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7d320-111">Return value</span></span>

<span data-ttu-id="7d320-112">Tipo: **objeto**</span><span class="sxs-lookup"><span data-stu-id="7d320-112">Type: **Object**</span></span>

<span data-ttu-id="7d320-113">Retorna uma expressão de objeto que é avaliada como o objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) do usuário.</span><span class="sxs-lookup"><span data-stu-id="7d320-113">Returns an object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d320-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d320-114">Remarks</span></span>

<span data-ttu-id="7d320-115">O sistema de arquivos NTFS cria automaticamente uma entrada de cota de usuário quando um usuário grava pela primeira vez no volume.</span><span class="sxs-lookup"><span data-stu-id="7d320-115">The NTFS file system automatically creates a user quota entry when a user first writes to the volume.</span></span> <span data-ttu-id="7d320-116">As entradas criadas dessa forma recebem o limite de aviso padrão e os valores de limite de cota rígido para o volume.</span><span class="sxs-lookup"><span data-stu-id="7d320-116">Entries that are created in this way are assigned the default warning threshold and hard quota limit values for the volume.</span></span> <span data-ttu-id="7d320-117">Esse método permite que você crie uma entrada de cota de usuário antes que um usuário grave informações no volume.</span><span class="sxs-lookup"><span data-stu-id="7d320-117">This method allows you to create a user quota entry before a user writes information to the volume.</span></span> <span data-ttu-id="7d320-118">Ele retorna um objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) que pode ser usado para atribuir um limite de aviso ou um valor de limite de cota que difere das configurações padrão para o volume.</span><span class="sxs-lookup"><span data-stu-id="7d320-118">It returns a [**DIDiskQuotaUser**](didiskquotauser-object.md) object that can be used to assign a warning threshold or quota limit value that differs from the default settings for the volume.</span></span>

<span data-ttu-id="7d320-119">Se o usuário já existir, nenhuma nova entrada será criada.</span><span class="sxs-lookup"><span data-stu-id="7d320-119">If the user already exists, no new entry is created.</span></span> <span data-ttu-id="7d320-120">O método retorna o objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) associado à entrada existente.</span><span class="sxs-lookup"><span data-stu-id="7d320-120">The method returns the [**DIDiskQuotaUser**](didiskquotauser-object.md) object associated with the existing entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d320-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d320-121">Requirements</span></span>



| <span data-ttu-id="7d320-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d320-122">Requirement</span></span> | <span data-ttu-id="7d320-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7d320-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d320-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d320-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7d320-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7d320-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7d320-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d320-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7d320-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7d320-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7d320-128">DLL</span><span class="sxs-lookup"><span data-stu-id="7d320-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d320-129"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="7d320-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d320-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d320-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d320-131">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="7d320-131">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="7d320-132">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="7d320-132">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[<span data-ttu-id="7d320-133">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="7d320-133">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




