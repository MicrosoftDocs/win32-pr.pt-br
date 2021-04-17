---
description: Grava o hive do registro offline especificado em um arquivo.
ms.assetid: 26f2eed9-e6e0-4dc0-8b91-212cde072744
title: Função ORSaveHive (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSaveHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 59df5b191a9bc0cfe98e1681665c5814935aa2c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748903"
---
# <a name="orsavehive-function"></a><span data-ttu-id="61c9f-103">Função ORSaveHive</span><span class="sxs-lookup"><span data-stu-id="61c9f-103">ORSaveHive function</span></span>

<span data-ttu-id="61c9f-104">Grava o hive do registro offline especificado em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="61c9f-104">Writes the specified offline registry hive to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="61c9f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61c9f-105">Syntax</span></span>


```C++
DWORD ORSaveHive(
  _In_ ORHKEY Handle,
  _In_ PCWSTR lpHivePath,
  _In_ DWORD  dwOsMajorVersion,
  _In_ DWORD  dwOsMinorVersion
);
```



## <a name="parameters"></a><span data-ttu-id="61c9f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61c9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61c9f-107">*Identificador* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="61c9f-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61c9f-108">Um identificador para o hive do registro offline a ser salvo.</span><span class="sxs-lookup"><span data-stu-id="61c9f-108">A handle to the offline registry hive to save.</span></span>

</dd> <dt>

<span data-ttu-id="61c9f-109">*lpHivePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="61c9f-109">*lpHivePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61c9f-110">Um ponteiro para uma cadeia de caracteres Unicode que especifica o nome do arquivo do hive do registro.</span><span class="sxs-lookup"><span data-stu-id="61c9f-110">A pointer to a Unicode string that specifies the name of the registry hive file.</span></span> <span data-ttu-id="61c9f-111">Este não pode ser o nome de um arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="61c9f-111">This cannot be the name of an existing file.</span></span>

</dd> <dt>

<span data-ttu-id="61c9f-112">*dwOsMajorVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="61c9f-112">*dwOsMajorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61c9f-113">O número de versão principal do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="61c9f-113">The major version number of the operating system.</span></span> <span data-ttu-id="61c9f-114">Esse membro pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="61c9f-114">This member can be one of the following values.</span></span>



| <span data-ttu-id="61c9f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="61c9f-115">Value</span></span>                                                                        | <span data-ttu-id="61c9f-116">Significado</span><span class="sxs-lookup"><span data-stu-id="61c9f-116">Meaning</span></span>                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="61c9f-117"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="61c9f-117"><dt>5</dt></span></span> </dl> | <span data-ttu-id="61c9f-118">Se *dwOsMinorVersion* for 1, o sistema operacional será o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="61c9f-118">If *dwOsMinorVersion* is 1, the operating system is Windows XP.</span></span><br/> <span data-ttu-id="61c9f-119">Se o *dwOsMinorVersion* for 2, o sistema operacional será o windows Server 2003 R2, o windows Server 2003 ou o Windows XP Professional x64 Edition.</span><span class="sxs-lookup"><span data-stu-id="61c9f-119">If *dwOsMinorVersion* is 2, the operating system is Windows Server 2003 R2, Windows Server 2003, or Windows XP Professional x64 Edition.</span></span><br/> |
| <dl> <span data-ttu-id="61c9f-120"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="61c9f-120"><dt>6</dt></span></span> </dl> | <span data-ttu-id="61c9f-121">Se *dwOsMinorVersion* for 0, o sistema operacional será o windows Server 2008 ou o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="61c9f-121">If *dwOsMinorVersion* is 0, the operating system is Windows Server 2008 or Windows Vista.</span></span><br/> <span data-ttu-id="61c9f-122">Se *dwOsMinorVersion* for 1, o sistema operacional será o windows Server 2008 R2 ou o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="61c9f-122">If *dwOsMinorVersion* is 1, the operating system is Windows Server 2008 R2 or Windows 7.</span></span><br/>                       |



 

</dd> <dt>

<span data-ttu-id="61c9f-123">*dwOsMinorVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="61c9f-123">*dwOsMinorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61c9f-124">O número de versão secundária do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="61c9f-124">The minor version number of the operating system.</span></span> <span data-ttu-id="61c9f-125">Esse membro pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="61c9f-125">This member can be one of the following values.</span></span>



| <span data-ttu-id="61c9f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="61c9f-126">Value</span></span>                                                                        | <span data-ttu-id="61c9f-127">Significado</span><span class="sxs-lookup"><span data-stu-id="61c9f-127">Meaning</span></span>                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="61c9f-128"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="61c9f-128"><dt>0</dt></span></span> </dl> | <span data-ttu-id="61c9f-129">Se o *dwOsMajorVersion* for 6, o sistema operacional será o windows Server 2008 ou o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="61c9f-129">If *dwOsMajorVersion* is 6, the operating system is Windows Server 2008 or Windows Vista.</span></span><br/>                                                                                                                                          |
| <dl> <span data-ttu-id="61c9f-130"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="61c9f-130"><dt>1</dt></span></span> </dl> | <span data-ttu-id="61c9f-131">Se *dwOsMajorVersion* for 5, o sistema operacional será o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="61c9f-131">If *dwOsMajorVersion* is 5, the operating system is Windows XP.</span></span><br/> <span data-ttu-id="61c9f-132">Se o *dwOsMajorVersion* for 6, o sistema operacional será o windows Server 2008 R2 ou o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="61c9f-132">If *dwOsMajorVersion* is 6, the operating system is Windows Server 2008 R2 or Windows 7.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="61c9f-133"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="61c9f-133"><dt>2</dt></span></span> </dl> | <span data-ttu-id="61c9f-134">Se o *dwOsMajorVersion* for 5, o sistema operacional será o windows Server 2003 R2, o windows Server 2003 ou o Windows XP Professional x64 Edition.</span><span class="sxs-lookup"><span data-stu-id="61c9f-134">If *dwOsMajorVersion* is 5, the operating system is Windows Server 2003 R2, Windows Server 2003, or Windows XP Professional x64 Edition.</span></span> <br/> <span data-ttu-id="61c9f-135">Se *dwOsMajorVersion* for 6, o parâmetro *dwOsMinorVersion* deverá ser 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="61c9f-135">If *dwOsMajorVersion* is 6, the *dwOsMinorVersion* parameter must be 0 or 1.</span></span> <br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61c9f-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="61c9f-136">Return value</span></span>

<span data-ttu-id="61c9f-137">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="61c9f-137">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="61c9f-138">Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="61c9f-138">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="61c9f-139">Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.</span><span class="sxs-lookup"><span data-stu-id="61c9f-139">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="61c9f-140">Os códigos de erro possíveis incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="61c9f-140">Possible error codes include the following:</span></span>

-   <span data-ttu-id="61c9f-141">Se o chamador não tiver os direitos de acesso necessários para gravar o arquivo, a função retornará o \_ acesso ao erro \_ negado.</span><span class="sxs-lookup"><span data-stu-id="61c9f-141">If the caller does not have the necessary access rights to write the file, the function returns ERROR\_ACCESS\_DENIED.</span></span>
-   <span data-ttu-id="61c9f-142">Se o arquivo especificado já existir, a função retornará um erro \_ já \_ existe.</span><span class="sxs-lookup"><span data-stu-id="61c9f-142">If the specified file already exists, the function returns ERROR\_ALREADY\_EXISTS.</span></span>

## <a name="remarks"></a><span data-ttu-id="61c9f-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="61c9f-143">Remarks</span></span>

<span data-ttu-id="61c9f-144">A função **ORSaveHive** deve ser usada para salvar as alterações feitas em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="61c9f-144">The **ORSaveHive** function must be used to save changes made to an offline registry hive.</span></span> <span data-ttu-id="61c9f-145">As alterações não são preservadas até que **ORSaveHive** seja chamado para salvar o hive em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="61c9f-145">Changes are not preserved until **ORSaveHive** is called to save the hive to a file.</span></span>

<span data-ttu-id="61c9f-146">Os parâmetros *dwOsMajorVersion* e *dwOsMinorVersion* juntos especificam o formato de destino do arquivo hive do registro.</span><span class="sxs-lookup"><span data-stu-id="61c9f-146">The *dwOsMajorVersion* and *dwOsMinorVersion* parameters together specify the target format of the registry hive file.</span></span> <span data-ttu-id="61c9f-147">A tabela a seguir resume os números de versão mais recentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="61c9f-147">The following table summarizes the most recent operating system version numbers.</span></span>



| <span data-ttu-id="61c9f-148">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="61c9f-148">Operating system</span></span>                    | <span data-ttu-id="61c9f-149">Número de versão</span><span class="sxs-lookup"><span data-stu-id="61c9f-149">Version number</span></span> |
|-------------------------------------|----------------|
| <span data-ttu-id="61c9f-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="61c9f-150">Windows Server 2008 R2</span></span>              | <span data-ttu-id="61c9f-151">6.1</span><span class="sxs-lookup"><span data-stu-id="61c9f-151">6.1</span></span>            |
| <span data-ttu-id="61c9f-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="61c9f-152">Windows 7</span></span>                           | <span data-ttu-id="61c9f-153">6.1</span><span class="sxs-lookup"><span data-stu-id="61c9f-153">6.1</span></span>            |
| <span data-ttu-id="61c9f-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61c9f-154">Windows Server 2008</span></span>                 | <span data-ttu-id="61c9f-155">6.0</span><span class="sxs-lookup"><span data-stu-id="61c9f-155">6.0</span></span>            |
| <span data-ttu-id="61c9f-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61c9f-156">Windows Vista</span></span>                       | <span data-ttu-id="61c9f-157">6.0</span><span class="sxs-lookup"><span data-stu-id="61c9f-157">6.0</span></span>            |
| <span data-ttu-id="61c9f-158">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="61c9f-158">Windows Server 2003 R2</span></span>              | <span data-ttu-id="61c9f-159">5.2</span><span class="sxs-lookup"><span data-stu-id="61c9f-159">5.2</span></span>            |
| <span data-ttu-id="61c9f-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="61c9f-160">Windows Server 2003</span></span>                 | <span data-ttu-id="61c9f-161">5.2</span><span class="sxs-lookup"><span data-stu-id="61c9f-161">5.2</span></span>            |
| <span data-ttu-id="61c9f-162">Windows XP Professional x64 Edition</span><span class="sxs-lookup"><span data-stu-id="61c9f-162">Windows XP Professional x64 Edition</span></span> | <span data-ttu-id="61c9f-163">5.2</span><span class="sxs-lookup"><span data-stu-id="61c9f-163">5.2</span></span>            |
| <span data-ttu-id="61c9f-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="61c9f-164">Windows XP</span></span>                          | <span data-ttu-id="61c9f-165">5.1</span><span class="sxs-lookup"><span data-stu-id="61c9f-165">5.1</span></span>            |



 

<span data-ttu-id="61c9f-166">Use a função [GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) para recuperar informações sobre o sistema operacional atual.</span><span class="sxs-lookup"><span data-stu-id="61c9f-166">Use the [GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) function to retrieve information about the current operating system.</span></span>

<span data-ttu-id="61c9f-167">A função **ORSaveHive** bloqueia o hive do registro enquanto está gravando o hive no arquivo e, em seguida, fecha o arquivo e libera o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="61c9f-167">The **ORSaveHive** function locks the registry hive while it is writing the hive to the file, then closes the file and releases the lock.</span></span> <span data-ttu-id="61c9f-168">O hive do registro permanece na memória até que seja fechado chamando a função [**ORCloseHive**](orclosehive.md) .</span><span class="sxs-lookup"><span data-stu-id="61c9f-168">The registry hive remains in memory until it is closed by calling the [**ORCloseHive**](orclosehive.md) function.</span></span> <span data-ttu-id="61c9f-169">É possível fazer outras alterações no hive do registro enquanto ele estiver aberto; no entanto, para preservar essas alterações, o hive deve ser salvo em um novo arquivo, pois a função **ORSaveHive** não substituirá um arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="61c9f-169">It is possible to make further changes to the registry hive while it is open; however, to preserve these changes the hive must be saved to a new file, because the **ORSaveHive** function will not overwrite an existing file.</span></span>

<span data-ttu-id="61c9f-170">A função **ORSaveHive** pode ser usada para salvar parte do hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="61c9f-170">The **ORSaveHive** function can be used to save part of the offline registry hive.</span></span> <span data-ttu-id="61c9f-171">A chave especificada no parâmetro *Handle* se torna a chave raiz de um Hive que consiste na chave especificada e todas as suas subchaves.</span><span class="sxs-lookup"><span data-stu-id="61c9f-171">The key specified in the *Handle* parameter becomes the root key of a hive that consists of the specified key and all of its subkeys.</span></span>

## <a name="requirements"></a><span data-ttu-id="61c9f-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61c9f-172">Requirements</span></span>



| <span data-ttu-id="61c9f-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="61c9f-173">Requirement</span></span> | <span data-ttu-id="61c9f-174">Valor</span><span class="sxs-lookup"><span data-stu-id="61c9f-174">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61c9f-175">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="61c9f-175">Redistributable</span></span><br/> | <span data-ttu-id="61c9f-176">Biblioteca de registro offline do Windows versão 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="61c9f-176">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="61c9f-177">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61c9f-177">Header</span></span><br/>          | <dl> <span data-ttu-id="61c9f-178"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="61c9f-178"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="61c9f-179">DLL</span><span class="sxs-lookup"><span data-stu-id="61c9f-179">DLL</span></span><br/>             | <dl> <span data-ttu-id="61c9f-180"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61c9f-180"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61c9f-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="61c9f-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61c9f-182">GetVersionEx</span><span class="sxs-lookup"><span data-stu-id="61c9f-182">GetVersionEx</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> <dt>

[<span data-ttu-id="61c9f-183">**ORCloseHive**</span><span class="sxs-lookup"><span data-stu-id="61c9f-183">**ORCloseHive**</span></span>](orclosehive.md)
</dt> <dt>

[<span data-ttu-id="61c9f-184">**OROpenHive**</span><span class="sxs-lookup"><span data-stu-id="61c9f-184">**OROpenHive**</span></span>](oropenhive.md)
</dt> </dl>

 

 
