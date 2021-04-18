---
description: Carrega o arquivo do hive do registro especificado na memória e valida o hive.
ms.assetid: 5d8498b0-e1bb-4c3d-bf3d-7bfc3002eb1a
title: Função OROpenHive (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ba6531e7a2ab2b0b148065d9f4666812e75f2968
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749409"
---
# <a name="oropenhive-function"></a><span data-ttu-id="674e8-103">Função OROpenHive</span><span class="sxs-lookup"><span data-stu-id="674e8-103">OROpenHive function</span></span>

<span data-ttu-id="674e8-104">Carrega o arquivo do hive do registro especificado na memória e valida o hive.</span><span class="sxs-lookup"><span data-stu-id="674e8-104">Loads the specified registry hive file into memory and validates the hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="674e8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="674e8-105">Syntax</span></span>


```C++
DWORD OROpenHive(
  _In_  PCWSTR  lpHivePath,
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a><span data-ttu-id="674e8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="674e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="674e8-107">*lpHivePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="674e8-107">*lpHivePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="674e8-108">Um ponteiro para uma cadeia de caracteres Unicode que especifica o nome do arquivo do hive do registro a ser carregado na memória.</span><span class="sxs-lookup"><span data-stu-id="674e8-108">A pointer to a Unicode string that specifies the name of the registry hive file to be loaded into memory.</span></span> <span data-ttu-id="674e8-109">Pode ser um arquivo de Hive que foi salvo com a função [**ORSaveHive**](orsavehive.md) ou criado com a função [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) ou [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) .</span><span class="sxs-lookup"><span data-stu-id="674e8-109">This can be a hive file that was saved with the [**ORSaveHive**](orsavehive.md) function or created with the [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) or [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) function.</span></span> <span data-ttu-id="674e8-110">O arquivo deve ter menos de 4 GB de tamanho e o chamador deve ter acesso de \_ dados de leitura de arquivo \_ ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="674e8-110">The file must be less than 4 GB in size, and the caller must have FILE\_READ\_DATA access to the file.</span></span> <span data-ttu-id="674e8-111">Para obter mais informações, consulte [segurança de arquivos e direitos de acesso](../fileio/file-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="674e8-111">For more information, see [File Security and Access Rights](../fileio/file-security-and-access-rights.md).</span></span>

</dd> <dt>

<span data-ttu-id="674e8-112">*phkResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="674e8-112">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="674e8-113">Um ponteiro para uma variável que recebe um identificador para a chave raiz do hive do registro offline carregado.</span><span class="sxs-lookup"><span data-stu-id="674e8-113">A pointer to a variable that receives a handle to the root key of the loaded offline registry hive.</span></span> <span data-ttu-id="674e8-114">Se o arquivo do hive do registro não puder ser aberto ou a validação falhar, a função definirá esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="674e8-114">If the registry hive file cannot be opened or validation fails, the function sets this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="674e8-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="674e8-115">Return value</span></span>

<span data-ttu-id="674e8-116">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="674e8-116">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="674e8-117">Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="674e8-117">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="674e8-118">Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.</span><span class="sxs-lookup"><span data-stu-id="674e8-118">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="674e8-119">Os códigos de erro possíveis incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="674e8-119">Possible error codes include the following:</span></span>

-   <span data-ttu-id="674e8-120">Se o arquivo estiver vazio ou tiver mais de 4 GB de tamanho, a função retornará o erro \_ BADDB.</span><span class="sxs-lookup"><span data-stu-id="674e8-120">If the file is empty or larger than 4 GB in size, the function returns ERROR\_BADDB.</span></span>
-   <span data-ttu-id="674e8-121">Se o chamador não tiver os direitos de acesso necessários para abrir o arquivo, a função retornará o \_ acesso ao erro \_ negado.</span><span class="sxs-lookup"><span data-stu-id="674e8-121">If the caller does not have the necessary access rights to open the file, the function returns ERROR\_ACCESS\_DENIED.</span></span>
-   <span data-ttu-id="674e8-122">Se o hive do registro falhar na validação, a função retornará um erro \_ não \_ arquivo de registro \_ .</span><span class="sxs-lookup"><span data-stu-id="674e8-122">If the registry hive fails validation, the function returns ERROR\_NOT\_REGISTRY\_FILE.</span></span>

## <a name="remarks"></a><span data-ttu-id="674e8-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="674e8-123">Remarks</span></span>

<span data-ttu-id="674e8-124">A função **OROpenHive** é a única função de registro offline que valida um hive do registro.</span><span class="sxs-lookup"><span data-stu-id="674e8-124">The **OROpenHive** function is the only offline registry function that validates a registry hive.</span></span> <span data-ttu-id="674e8-125">Se a validação falhar, nenhuma tentativa será feita para reparar o hive.</span><span class="sxs-lookup"><span data-stu-id="674e8-125">If the validation fails, no attempt is made to repair the hive.</span></span>

## <a name="requirements"></a><span data-ttu-id="674e8-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="674e8-126">Requirements</span></span>



| <span data-ttu-id="674e8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="674e8-127">Requirement</span></span> | <span data-ttu-id="674e8-128">Valor</span><span class="sxs-lookup"><span data-stu-id="674e8-128">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="674e8-129">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="674e8-129">Redistributable</span></span><br/> | <span data-ttu-id="674e8-130">Biblioteca de registro offline do Windows versão 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="674e8-130">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="674e8-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="674e8-131">Header</span></span><br/>          | <dl> <span data-ttu-id="674e8-132"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="674e8-132"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="674e8-133">DLL</span><span class="sxs-lookup"><span data-stu-id="674e8-133">DLL</span></span><br/>             | <dl> <span data-ttu-id="674e8-134"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="674e8-134"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="674e8-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="674e8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="674e8-136">**ORCloseHive**</span><span class="sxs-lookup"><span data-stu-id="674e8-136">**ORCloseHive**</span></span>](orclosehive.md)
</dt> <dt>

[<span data-ttu-id="674e8-137">**ORCreateHive**</span><span class="sxs-lookup"><span data-stu-id="674e8-137">**ORCreateHive**</span></span>](orcreatehive.md)
</dt> <dt>

[<span data-ttu-id="674e8-138">**ORSaveHive**</span><span class="sxs-lookup"><span data-stu-id="674e8-138">**ORSaveHive**</span></span>](orsavehive.md)
</dt> <dt>

[<span data-ttu-id="674e8-139">RegSaveKey</span><span class="sxs-lookup"><span data-stu-id="674e8-139">RegSaveKey</span></span>](/windows/win32/api/winreg/nf-winreg-regsavekeya)
</dt> <dt>

[<span data-ttu-id="674e8-140">RegSaveKeyEx</span><span class="sxs-lookup"><span data-stu-id="674e8-140">RegSaveKeyEx</span></span>](/windows/win32/api/winreg/nf-winreg-regsavekeyexa)
</dt> </dl>

 

 
