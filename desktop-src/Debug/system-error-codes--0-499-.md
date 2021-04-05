---
description: Descreve os códigos de erro 0-499 definidos no arquivo de cabeçalho WinError. h e destina-se a desenvolvedores.
ms.assetid: cacb0aec-d438-4875-a96e-4e0239fdc6ba
title: Códigos de erro do sistema (0-499) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 413d9674f511bd49df12267b60d6c6c3dac366aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826432"
---
# <a name="system-error-codes-0-499"></a><span data-ttu-id="9cec1-103">Códigos de erro do sistema (0-499)</span><span class="sxs-lookup"><span data-stu-id="9cec1-103">System Error Codes (0-499)</span></span>

> [!NOTE]
> <span data-ttu-id="9cec1-104">Essas informações destinam-se a desenvolvedores Depurando erros do sistema.</span><span class="sxs-lookup"><span data-stu-id="9cec1-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="9cec1-105">Para outros erros, como problemas com Windows Update, há uma lista de recursos na página códigos de [erro](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="9cec1-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="9cec1-106">A lista a seguir descreve os [códigos de erro do sistema](system-error-codes.md) (erros 0 a 499).</span><span class="sxs-lookup"><span data-stu-id="9cec1-106">The following list describes [system error codes](system-error-codes.md) (errors 0 to 499).</span></span> <span data-ttu-id="9cec1-107">Elas são retornadas pela função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando muitas funções falham.</span><span class="sxs-lookup"><span data-stu-id="9cec1-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="9cec1-108">Para recuperar o texto de descrição do erro em seu aplicativo, use a função [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com a **mensagem de formato \_ \_ do sinalizador do \_ sistema** .</span><span class="sxs-lookup"><span data-stu-id="9cec1-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="9cec1-109"><span id="ERROR_SUCCESS"></span><span id="error_success"></span>**êxito do erro \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-109"><span id="ERROR_SUCCESS"></span><span id="error_success"></span>**ERROR\_SUCCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-110">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="9cec1-110">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-111">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="9cec1-111">The operation completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-112"><span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**função de erro \_ inválida \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-112"><span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**ERROR\_INVALID\_FUNCTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-113">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="9cec1-113">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-114">Função incorreta.</span><span class="sxs-lookup"><span data-stu-id="9cec1-114">Incorrect function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-115"><span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**arquivo de erro \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-115"><span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**ERROR\_FILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-116">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="9cec1-116">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-117">O sistema não pode encontrar o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-117">The system cannot find the file specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-118"><span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**caminho de erro \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-118"><span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**ERROR\_PATH\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-119">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="9cec1-119">3 (0x3)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-120">O sistema não pode localizar o caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-120">The system cannot find the path specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-121"><span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**ERRO \_ em \_ muitos \_ \_ arquivos abertos**</span><span class="sxs-lookup"><span data-stu-id="9cec1-121"><span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**ERROR\_TOO\_MANY\_OPEN\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-122">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="9cec1-122">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-123">O sistema não pode abrir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="9cec1-123">The system cannot open the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-124"><span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**ERRO de \_ acesso \_ negado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-124"><span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-125">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="9cec1-125">5 (0x5)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-126">O acesso foi negado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-126">Access is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-127"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**\_identificador inválido do erro \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-127"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR\_INVALID\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-128">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="9cec1-128">6 (0x6)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-129">O manipulador é inválido.</span><span class="sxs-lookup"><span data-stu-id="9cec1-129">The handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-130"><span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**Arena de erro em \_ \_ Trash**</span><span class="sxs-lookup"><span data-stu-id="9cec1-130"><span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**ERROR\_ARENA\_TRASHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-131">7 (0x7)</span><span class="sxs-lookup"><span data-stu-id="9cec1-131">7 (0x7)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-132">Os blocos de controle de armazenamento foram destruídos.</span><span class="sxs-lookup"><span data-stu-id="9cec1-132">The storage control blocks were destroyed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-133"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERRO \_ de \_ memória insuficiente \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-133"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-134">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="9cec1-134">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-135">Não há recursos de memória suficientes disponíveis para processar este comando.</span><span class="sxs-lookup"><span data-stu-id="9cec1-135">Not enough memory resources are available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-136"><span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**ERRO \_ de \_ bloco inválido**</span><span class="sxs-lookup"><span data-stu-id="9cec1-136"><span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**ERROR\_INVALID\_BLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-137">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="9cec1-137">9 (0x9)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-138">O endereço do bloco de controle de armazenamento é inválido.</span><span class="sxs-lookup"><span data-stu-id="9cec1-138">The storage control block address is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-139"><span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**ERRO \_ de \_ ambiente insatisfatório**</span><span class="sxs-lookup"><span data-stu-id="9cec1-139"><span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**ERROR\_BAD\_ENVIRONMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-140">10 (0xA)</span><span class="sxs-lookup"><span data-stu-id="9cec1-140">10 (0xA)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-141">O ambiente está incorreto.</span><span class="sxs-lookup"><span data-stu-id="9cec1-141">The environment is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-142"><span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**ERRO \_ de \_ formato inadequado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-142"><span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**ERROR\_BAD\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-143">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="9cec1-143">11 (0xB)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-144">Foi feita uma tentativa de carregar um programa com um formato incorreto.</span><span class="sxs-lookup"><span data-stu-id="9cec1-144">An attempt was made to load a program with an incorrect format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-145"><span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**ERRO \_ de \_ acesso inválido**</span><span class="sxs-lookup"><span data-stu-id="9cec1-145"><span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**ERROR\_INVALID\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-146">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="9cec1-146">12 (0xC)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-147">O código de acesso é inválido.</span><span class="sxs-lookup"><span data-stu-id="9cec1-147">The access code is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-148"><span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**ERRO de \_ dados inválidos \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-148"><span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**ERROR\_INVALID\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-149">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="9cec1-149">13 (0xD)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-150">Os dados são inválidos.</span><span class="sxs-lookup"><span data-stu-id="9cec1-150">The data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-151"><span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**ERRO \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="9cec1-151"><span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**ERROR\_OUTOFMEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-152">14 (0xE)</span><span class="sxs-lookup"><span data-stu-id="9cec1-152">14 (0xE)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-153">Não há armazenamento suficiente disponível para concluir esta operação.</span><span class="sxs-lookup"><span data-stu-id="9cec1-153">Not enough storage is available to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-154"><span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**ERRO \_ de \_ unidade inválida**</span><span class="sxs-lookup"><span data-stu-id="9cec1-154"><span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**ERROR\_INVALID\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-155">15 (0xF)</span><span class="sxs-lookup"><span data-stu-id="9cec1-155">15 (0xF)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-156">O sistema não pode localizar a unidade especificada.</span><span class="sxs-lookup"><span data-stu-id="9cec1-156">The system cannot find the drive specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-157"><span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**ERRO \_ no \_ diretório atual**</span><span class="sxs-lookup"><span data-stu-id="9cec1-157"><span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**ERROR\_CURRENT\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-158">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="9cec1-158">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-159">O diretório não pode ser removido.</span><span class="sxs-lookup"><span data-stu-id="9cec1-159">The directory cannot be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-160"><span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**ERRO \_ não no \_ mesmo \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="9cec1-160"><span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**ERROR\_NOT\_SAME\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-161">17 (0x11)</span><span class="sxs-lookup"><span data-stu-id="9cec1-161">17 (0x11)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-162">O sistema não pode mover o arquivo para uma unidade de disco diferente.</span><span class="sxs-lookup"><span data-stu-id="9cec1-162">The system cannot move the file to a different disk drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-163"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERRO \_ não há \_ mais \_ arquivos**</span><span class="sxs-lookup"><span data-stu-id="9cec1-163"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR\_NO\_MORE\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-164">18 (0x12)</span><span class="sxs-lookup"><span data-stu-id="9cec1-164">18 (0x12)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-165">Não há mais arquivos.</span><span class="sxs-lookup"><span data-stu-id="9cec1-165">There are no more files.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-166"><span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**ERRO \_ de \_ proteção contra gravação**</span><span class="sxs-lookup"><span data-stu-id="9cec1-166"><span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**ERROR\_WRITE\_PROTECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-167">19 (0x13)</span><span class="sxs-lookup"><span data-stu-id="9cec1-167">19 (0x13)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-168">A mídia está protegida contra gravação.</span><span class="sxs-lookup"><span data-stu-id="9cec1-168">The media is write protected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-169"><span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**ERRO \_ de \_ unidade inadequada**</span><span class="sxs-lookup"><span data-stu-id="9cec1-169"><span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**ERROR\_BAD\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-170">20 (0x14)</span><span class="sxs-lookup"><span data-stu-id="9cec1-170">20 (0x14)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-171">O sistema não pode localizar o dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-171">The system cannot find the device specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-172"><span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**ERRO \_ não \_ está pronto**</span><span class="sxs-lookup"><span data-stu-id="9cec1-172"><span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**ERROR\_NOT\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-173">21 (0x15)</span><span class="sxs-lookup"><span data-stu-id="9cec1-173">21 (0x15)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-174">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="9cec1-174">The device is not ready.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-175"><span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**ERRO \_ de \_ comando insatisfatório**</span><span class="sxs-lookup"><span data-stu-id="9cec1-175"><span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**ERROR\_BAD\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-176">22 (0x16)</span><span class="sxs-lookup"><span data-stu-id="9cec1-176">22 (0x16)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-177">O dispositivo não reconhece o comando.</span><span class="sxs-lookup"><span data-stu-id="9cec1-177">The device does not recognize the command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-178"><span id="ERROR_CRC"></span><span id="error_crc"></span>**ERRO de \_ CRC**</span><span class="sxs-lookup"><span data-stu-id="9cec1-178"><span id="ERROR_CRC"></span><span id="error_crc"></span>**ERROR\_CRC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-179">23 (0x17)</span><span class="sxs-lookup"><span data-stu-id="9cec1-179">23 (0x17)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-180">Erro de dados (verificação de redundância cíclica).</span><span class="sxs-lookup"><span data-stu-id="9cec1-180">Data error (cyclic redundancy check).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-181"><span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**ERRO \_ de \_ comprimento insatisfatório**</span><span class="sxs-lookup"><span data-stu-id="9cec1-181"><span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**ERROR\_BAD\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-182">24 (0x18)</span><span class="sxs-lookup"><span data-stu-id="9cec1-182">24 (0x18)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-183">O programa emitiu um comando, mas o comprimento do comando está incorreto.</span><span class="sxs-lookup"><span data-stu-id="9cec1-183">The program issued a command but the command length is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-184"><span id="ERROR_SEEK"></span><span id="error_seek"></span>**ERRO de \_ busca**</span><span class="sxs-lookup"><span data-stu-id="9cec1-184"><span id="ERROR_SEEK"></span><span id="error_seek"></span>**ERROR\_SEEK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-185">25 (0x19)</span><span class="sxs-lookup"><span data-stu-id="9cec1-185">25 (0x19)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-186">A unidade não pode localizar uma área ou trilha específica no disco.</span><span class="sxs-lookup"><span data-stu-id="9cec1-186">The drive cannot locate a specific area or track on the disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-187"><span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**ERRO \_ não \_ \_ disco dos**</span><span class="sxs-lookup"><span data-stu-id="9cec1-187"><span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**ERROR\_NOT\_DOS\_DISK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-188">26 (0x1A)</span><span class="sxs-lookup"><span data-stu-id="9cec1-188">26 (0x1A)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-189">O disco ou disquete especificado não pode ser acessado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-189">The specified disk or diskette cannot be accessed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-190"><span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**setor de erro \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-190"><span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**ERROR\_SECTOR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-191">27 (0x1B)</span><span class="sxs-lookup"><span data-stu-id="9cec1-191">27 (0x1B)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-192">A unidade não pode localizar o setor solicitado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-192">The drive cannot find the sector requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-193"><span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**ERRO \_ sem \_ \_ papel**</span><span class="sxs-lookup"><span data-stu-id="9cec1-193"><span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**ERROR\_OUT\_OF\_PAPER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-194">28 (0x1C)</span><span class="sxs-lookup"><span data-stu-id="9cec1-194">28 (0x1C)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-195">A impressora está sem papel.</span><span class="sxs-lookup"><span data-stu-id="9cec1-195">The printer is out of paper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-196"><span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**\_falha de gravação de erro \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-196"><span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**ERROR\_WRITE\_FAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-197">29 (0x1D)</span><span class="sxs-lookup"><span data-stu-id="9cec1-197">29 (0x1D)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-198">O sistema não pode gravar no dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-198">The system cannot write to the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-199"><span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**\_falha de leitura de erro \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-199"><span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**ERROR\_READ\_FAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-200">30 (0x1E)</span><span class="sxs-lookup"><span data-stu-id="9cec1-200">30 (0x1E)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-201">O sistema não pode ler do dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-201">The system cannot read from the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-202"><span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**\_falha de Gen de erro \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-202"><span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**ERROR\_GEN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-203">31 (0x1F)</span><span class="sxs-lookup"><span data-stu-id="9cec1-203">31 (0x1F)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-204">Um dispositivo conectado ao sistema não está funcionando.</span><span class="sxs-lookup"><span data-stu-id="9cec1-204">A device attached to the system is not functioning.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-205"><span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**\_violação de compartilhamento de erro \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-205"><span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**ERROR\_SHARING\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-206">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="9cec1-206">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-207">O processo não pode acessar o arquivo porque ele está sendo usado por outro processo.</span><span class="sxs-lookup"><span data-stu-id="9cec1-207">The process cannot access the file because it is being used by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-208"><span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**\_violação de bloqueio de erro \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-208"><span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**ERROR\_LOCK\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-209">33 (0x21)</span><span class="sxs-lookup"><span data-stu-id="9cec1-209">33 (0x21)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-210">O processo não pode acessar o arquivo porque outro processo bloqueou uma parte dele.</span><span class="sxs-lookup"><span data-stu-id="9cec1-210">The process cannot access the file because another process has locked a portion of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-211"><span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**ERRO \_ de \_ disco incorreto**</span><span class="sxs-lookup"><span data-stu-id="9cec1-211"><span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**ERROR\_WRONG\_DISK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-212">34 (0x22)</span><span class="sxs-lookup"><span data-stu-id="9cec1-212">34 (0x22)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-213">O disquete errado está na unidade.</span><span class="sxs-lookup"><span data-stu-id="9cec1-213">The wrong diskette is in the drive.</span></span> <span data-ttu-id="9cec1-214">Insira %2 (número de série do volume: %3) na unidade %1.</span><span class="sxs-lookup"><span data-stu-id="9cec1-214">Insert %2 (Volume Serial Number: %3) into drive %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-215"><span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**o \_ buffer de compartilhamento de erro \_ \_ foi excedido**</span><span class="sxs-lookup"><span data-stu-id="9cec1-215"><span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**ERROR\_SHARING\_BUFFER\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-216">36 (0x24)</span><span class="sxs-lookup"><span data-stu-id="9cec1-216">36 (0x24)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-217">Muitos arquivos abertos para compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="9cec1-217">Too many files opened for sharing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-218"><span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**identificador de erro \_ \_ EOF**</span><span class="sxs-lookup"><span data-stu-id="9cec1-218"><span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**ERROR\_HANDLE\_EOF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-219">38 (0x26)</span><span class="sxs-lookup"><span data-stu-id="9cec1-219">38 (0x26)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-220">Fim do arquivo atingido.</span><span class="sxs-lookup"><span data-stu-id="9cec1-220">Reached the end of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-221"><span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**ERRO de \_ identificador de \_ disco \_ cheio**</span><span class="sxs-lookup"><span data-stu-id="9cec1-221"><span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**ERROR\_HANDLE\_DISK\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-222">39 (0x27)</span><span class="sxs-lookup"><span data-stu-id="9cec1-222">39 (0x27)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-223">O disco está cheio.</span><span class="sxs-lookup"><span data-stu-id="9cec1-223">The disk is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-224"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERRO \_ sem \_ suporte**</span><span class="sxs-lookup"><span data-stu-id="9cec1-224"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERROR\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-225">50 (0x32)</span><span class="sxs-lookup"><span data-stu-id="9cec1-225">50 (0x32)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-226">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="9cec1-226">The request is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-227"><span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**ERRO \_ REM \_ não \_ lista**</span><span class="sxs-lookup"><span data-stu-id="9cec1-227"><span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**ERROR\_REM\_NOT\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-228">51 (0x33)</span><span class="sxs-lookup"><span data-stu-id="9cec1-228">51 (0x33)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-229">O Windows não pode localizar o caminho de rede.</span><span class="sxs-lookup"><span data-stu-id="9cec1-229">Windows cannot find the network path.</span></span> <span data-ttu-id="9cec1-230">Verifique se o caminho de rede está correto e se o computador de destino não está ocupado ou desligado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-230">Verify that the network path is correct and the destination computer is not busy or turned off.</span></span> <span data-ttu-id="9cec1-231">Se o Windows ainda não conseguir localizar o caminho de rede, entre em contato com o administrador da rede.</span><span class="sxs-lookup"><span data-stu-id="9cec1-231">If Windows still cannot find the network path, contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-232"><span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**\_nome do Dup de erro \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-232"><span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**ERROR\_DUP\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-233">52 (0x34)</span><span class="sxs-lookup"><span data-stu-id="9cec1-233">52 (0x34)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-234">Você não estava conectado porque existe um nome duplicado na rede.</span><span class="sxs-lookup"><span data-stu-id="9cec1-234">You were not connected because a duplicate name exists on the network.</span></span> <span data-ttu-id="9cec1-235">Se estiver ingressando em um domínio, vá para sistema no painel de controle para alterar o nome do computador e tente novamente.</span><span class="sxs-lookup"><span data-stu-id="9cec1-235">If joining a domain, go to System in Control Panel to change the computer name and try again.</span></span> <span data-ttu-id="9cec1-236">Se estiver ingressando em um grupo de trabalho, escolha outro nome de grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9cec1-236">If joining a workgroup, choose another workgroup name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-237"><span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**ERRO \_ de \_ netpath insatisfatório**</span><span class="sxs-lookup"><span data-stu-id="9cec1-237"><span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**ERROR\_BAD\_NETPATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-238">53 (0x35)</span><span class="sxs-lookup"><span data-stu-id="9cec1-238">53 (0x35)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-239">O caminho da rede não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-239">The network path was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-240"><span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**ERRO de \_ rede \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-240"><span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**ERROR\_NETWORK\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-241">54 (0x36)</span><span class="sxs-lookup"><span data-stu-id="9cec1-241">54 (0x36)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-242">A rede está ocupada.</span><span class="sxs-lookup"><span data-stu-id="9cec1-242">The network is busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-243"><span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**\_desenvolvimento de \_ erro \_ inexistente**</span><span class="sxs-lookup"><span data-stu-id="9cec1-243"><span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**ERROR\_DEV\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-244">55 (0x37)</span><span class="sxs-lookup"><span data-stu-id="9cec1-244">55 (0x37)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-245">O dispositivo ou recurso de rede especificado não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="9cec1-245">The specified network resource or device is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-246"><span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**ERRO em excesso de \_ \_ \_ cmds**</span><span class="sxs-lookup"><span data-stu-id="9cec1-246"><span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**ERROR\_TOO\_MANY\_CMDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-247">56 (0x38)</span><span class="sxs-lookup"><span data-stu-id="9cec1-247">56 (0x38)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-248">O limite de comandos do BIOS de rede foi atingido.</span><span class="sxs-lookup"><span data-stu-id="9cec1-248">The network BIOS command limit has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-249"><span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**ERRO \_ \_ HDW ADAP \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-249"><span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**ERROR\_ADAP\_HDW\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-250">57 (0x39)</span><span class="sxs-lookup"><span data-stu-id="9cec1-250">57 (0x39)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-251">Ocorreu um erro de hardware do adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="9cec1-251">A network adapter hardware error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-252"><span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**ERRO \_ \_ resp net inadequado \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-252"><span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**ERROR\_BAD\_NET\_RESP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-253">58 (0x3A)</span><span class="sxs-lookup"><span data-stu-id="9cec1-253">58 (0x3A)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-254">O servidor especificado não pode executar a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="9cec1-254">The specified server cannot perform the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-255"><span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**ERRO \_ UNEXP \_ net \_ Err**</span><span class="sxs-lookup"><span data-stu-id="9cec1-255"><span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**ERROR\_UNEXP\_NET\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-256">59 (0x3B)</span><span class="sxs-lookup"><span data-stu-id="9cec1-256">59 (0x3B)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-257">Ocorreu um erro de rede inesperado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-257">An unexpected network error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-258"><span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**ERRO \_ de \_ REM \_ .**</span><span class="sxs-lookup"><span data-stu-id="9cec1-258"><span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**ERROR\_BAD\_REM\_ADAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-259">60 (0x3C)</span><span class="sxs-lookup"><span data-stu-id="9cec1-259">60 (0x3C)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-260">O adaptador remoto não é compatível.</span><span class="sxs-lookup"><span data-stu-id="9cec1-260">The remote adapter is not compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-261"><span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**ERRO \_ PRINTQ \_ completo**</span><span class="sxs-lookup"><span data-stu-id="9cec1-261"><span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**ERROR\_PRINTQ\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-262">61 (0x3D)</span><span class="sxs-lookup"><span data-stu-id="9cec1-262">61 (0x3D)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-263">A fila de impressora está cheia.</span><span class="sxs-lookup"><span data-stu-id="9cec1-263">The printer queue is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-264"><span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**ERRO \_ nenhum \_ espaço de spool \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-264"><span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**ERROR\_NO\_SPOOL\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-265">62 (0x3E)</span><span class="sxs-lookup"><span data-stu-id="9cec1-265">62 (0x3E)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-266">O espaço para armazenar o arquivo que está aguardando para ser impresso não está disponível no servidor.</span><span class="sxs-lookup"><span data-stu-id="9cec1-266">Space to store the file waiting to be printed is not available on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-267"><span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**ERRO ao \_ Imprimir \_ cancelado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-267"><span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**ERROR\_PRINT\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-268">63 (0x3F)</span><span class="sxs-lookup"><span data-stu-id="9cec1-268">63 (0x3F)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-269">O arquivo aguardando para ser impresso foi excluído.</span><span class="sxs-lookup"><span data-stu-id="9cec1-269">Your file waiting to be printed was deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-270"><span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**ERRO \_ NetName \_ excluído**</span><span class="sxs-lookup"><span data-stu-id="9cec1-270"><span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**ERROR\_NETNAME\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-271">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="9cec1-271">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-272">O nome da rede especificado não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="9cec1-272">The specified network name is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-273"><span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**ERRO \_ de \_ acesso à rede \_ negado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-273"><span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**ERROR\_NETWORK\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-274">65 (0x41)</span><span class="sxs-lookup"><span data-stu-id="9cec1-274">65 (0x41)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-275">Acesso à rede negado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-275">Network access is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-276"><span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**ERRO \_ \_ tipo de desenvolvimento insatisfatório \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-276"><span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**ERROR\_BAD\_DEV\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-277">66 (0x42)</span><span class="sxs-lookup"><span data-stu-id="9cec1-277">66 (0x42)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-278">O tipo de recurso de rede não está correto.</span><span class="sxs-lookup"><span data-stu-id="9cec1-278">The network resource type is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-279"><span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**ERRO \_ de \_ nome de rede insatisfatório \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-279"><span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**ERROR\_BAD\_NET\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-280">67 (0x43)</span><span class="sxs-lookup"><span data-stu-id="9cec1-280">67 (0x43)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-281">O nome de rede não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-281">The network name cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-282"><span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**ERRO \_ em \_ muitos \_ nomes**</span><span class="sxs-lookup"><span data-stu-id="9cec1-282"><span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**ERROR\_TOO\_MANY\_NAMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-283">68 (0x44)</span><span class="sxs-lookup"><span data-stu-id="9cec1-283">68 (0x44)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-284">O limite de nome para a placa do adaptador de rede do computador local foi excedido.</span><span class="sxs-lookup"><span data-stu-id="9cec1-284">The name limit for the local computer network adapter card was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-285"><span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**ERRO em excesso de \_ \_ \_ sess**</span><span class="sxs-lookup"><span data-stu-id="9cec1-285"><span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**ERROR\_TOO\_MANY\_SESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-286">69 (0x45)</span><span class="sxs-lookup"><span data-stu-id="9cec1-286">69 (0x45)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-287">O limite de sessão do BIOS de rede foi excedido.</span><span class="sxs-lookup"><span data-stu-id="9cec1-287">The network BIOS session limit was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-288"><span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**ERRO ao \_ compartilhar em \_ pausa**</span><span class="sxs-lookup"><span data-stu-id="9cec1-288"><span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**ERROR\_SHARING\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-289">70 (0x46)</span><span class="sxs-lookup"><span data-stu-id="9cec1-289">70 (0x46)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-290">O servidor remoto foi pausado ou está em processo de ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-290">The remote server has been paused or is in the process of being started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-291"><span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**Req. de erro \_ \_ não \_ ACCEP**</span><span class="sxs-lookup"><span data-stu-id="9cec1-291"><span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**ERROR\_REQ\_NOT\_ACCEP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-292">71 (0x47)</span><span class="sxs-lookup"><span data-stu-id="9cec1-292">71 (0x47)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-293">Não é possível fazer mais conexões com este computador remoto no momento porque já existem tantas conexões quantas o computador pode aceitar.</span><span class="sxs-lookup"><span data-stu-id="9cec1-293">No more connections can be made to this remote computer at this time because there are already as many connections as the computer can accept.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-294"><span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**ERRO \_ REDIR em \_ pausa**</span><span class="sxs-lookup"><span data-stu-id="9cec1-294"><span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**ERROR\_REDIR\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-295">72 (0x48)</span><span class="sxs-lookup"><span data-stu-id="9cec1-295">72 (0x48)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-296">A impressora ou o dispositivo de disco especificado foi pausado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-296">The specified printer or disk device has been paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-297"><span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**o \_ arquivo de erro \_ existe**</span><span class="sxs-lookup"><span data-stu-id="9cec1-297"><span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**ERROR\_FILE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-298">80 (0x50)</span><span class="sxs-lookup"><span data-stu-id="9cec1-298">80 (0x50)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-299">O arquivo existe.</span><span class="sxs-lookup"><span data-stu-id="9cec1-299">The file exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-300"><span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**ERRO \_ não é possível \_ fazer**</span><span class="sxs-lookup"><span data-stu-id="9cec1-300"><span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**ERROR\_CANNOT\_MAKE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-301">82 (0x52)</span><span class="sxs-lookup"><span data-stu-id="9cec1-301">82 (0x52)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-302">Não é possível criar o diretório ou arquivo.</span><span class="sxs-lookup"><span data-stu-id="9cec1-302">The directory or file cannot be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-303"><span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**ERRO \_ falha \_ I24**</span><span class="sxs-lookup"><span data-stu-id="9cec1-303"><span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**ERROR\_FAIL\_I24**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-304">83 (0x53)</span><span class="sxs-lookup"><span data-stu-id="9cec1-304">83 (0x53)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-305">Falha em INT 24.</span><span class="sxs-lookup"><span data-stu-id="9cec1-305">Fail on INT 24.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-306"><span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**ERRO \_ fora \_ de \_ estruturas**</span><span class="sxs-lookup"><span data-stu-id="9cec1-306"><span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**ERROR\_OUT\_OF\_STRUCTURES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-307">84 (0x54)</span><span class="sxs-lookup"><span data-stu-id="9cec1-307">84 (0x54)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-308">O armazenamento para processar esta solicitação não está disponível.</span><span class="sxs-lookup"><span data-stu-id="9cec1-308">Storage to process this request is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-309"><span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**ERRO \_ já \_ atribuído**</span><span class="sxs-lookup"><span data-stu-id="9cec1-309"><span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**ERROR\_ALREADY\_ASSIGNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-310">85 (0x55)</span><span class="sxs-lookup"><span data-stu-id="9cec1-310">85 (0x55)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-311">O nome do dispositivo local já está em uso.</span><span class="sxs-lookup"><span data-stu-id="9cec1-311">The local device name is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-312"><span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**\_senha inválida do erro \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-312"><span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**ERROR\_INVALID\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-313">86 (0x56)</span><span class="sxs-lookup"><span data-stu-id="9cec1-313">86 (0x56)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-314">A senha da rede especificada não está correta.</span><span class="sxs-lookup"><span data-stu-id="9cec1-314">The specified network password is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-315"><span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**\_parâmetro inválido de erro \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-315"><span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-316">87 (0x57)</span><span class="sxs-lookup"><span data-stu-id="9cec1-316">87 (0x57)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-317">O parâmetro está incorreto.</span><span class="sxs-lookup"><span data-stu-id="9cec1-317">The parameter is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-318"><span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**ERRO \_ de \_ falha de gravação de rede \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-318"><span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**ERROR\_NET\_WRITE\_FAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-319">88 (0x58)</span><span class="sxs-lookup"><span data-stu-id="9cec1-319">88 (0x58)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-320">Ocorreu uma falha de gravação na rede.</span><span class="sxs-lookup"><span data-stu-id="9cec1-320">A write fault occurred on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-321"><span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**ERRO \_ sem \_ \_ Slots proc**</span><span class="sxs-lookup"><span data-stu-id="9cec1-321"><span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**ERROR\_NO\_PROC\_SLOTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-322">89 (0x59)</span><span class="sxs-lookup"><span data-stu-id="9cec1-322">89 (0x59)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-323">O sistema não pode iniciar outro processo no momento.</span><span class="sxs-lookup"><span data-stu-id="9cec1-323">The system cannot start another process at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-324"><span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**ERRO em excesso de \_ \_ \_ semáforos**</span><span class="sxs-lookup"><span data-stu-id="9cec1-324"><span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**ERROR\_TOO\_MANY\_SEMAPHORES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-325">100 (0x64)</span><span class="sxs-lookup"><span data-stu-id="9cec1-325">100 (0x64)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-326">Não é possível criar outro semáforo do sistema.</span><span class="sxs-lookup"><span data-stu-id="9cec1-326">Cannot create another system semaphore.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-327"><span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**ERRO \_ excl \_ sem \_ \_ Propriedade já pertencente**</span><span class="sxs-lookup"><span data-stu-id="9cec1-327"><span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**ERROR\_EXCL\_SEM\_ALREADY\_OWNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-328">101 (0x65)</span><span class="sxs-lookup"><span data-stu-id="9cec1-328">101 (0x65)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-329">O semáforo exclusivo pertence a outro processo.</span><span class="sxs-lookup"><span data-stu-id="9cec1-329">The exclusive semaphore is owned by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-330"><span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**o erro \_ sem \_ está \_ definido**</span><span class="sxs-lookup"><span data-stu-id="9cec1-330"><span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**ERROR\_SEM\_IS\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-331">102 (0x66)</span><span class="sxs-lookup"><span data-stu-id="9cec1-331">102 (0x66)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-332">O semáforo está definido e não pode ser fechado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-332">The semaphore is set and cannot be closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-333"><span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**ERRO \_ número \_ excessivo \_ de \_ solicitações sem**</span><span class="sxs-lookup"><span data-stu-id="9cec1-333"><span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**ERROR\_TOO\_MANY\_SEM\_REQUESTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-334">103 (0x67)</span><span class="sxs-lookup"><span data-stu-id="9cec1-334">103 (0x67)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-335">O semáforo não pode ser definido novamente.</span><span class="sxs-lookup"><span data-stu-id="9cec1-335">The semaphore cannot be set again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-336"><span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**ERRO \_ inválido \_ no \_ tempo de interrupção \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-336"><span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**ERROR\_INVALID\_AT\_INTERRUPT\_TIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-337">104 (0x68)</span><span class="sxs-lookup"><span data-stu-id="9cec1-337">104 (0x68)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-338">Não é possível solicitar semáforos exclusivos no tempo de interrupção.</span><span class="sxs-lookup"><span data-stu-id="9cec1-338">Cannot request exclusive semaphores at interrupt time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-339"><span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**ERRO \_ sem \_ proprietário \_ morreu**</span><span class="sxs-lookup"><span data-stu-id="9cec1-339"><span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**ERROR\_SEM\_OWNER\_DIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-340">105 (0x69)</span><span class="sxs-lookup"><span data-stu-id="9cec1-340">105 (0x69)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-341">A propriedade anterior deste semáforo foi encerrada.</span><span class="sxs-lookup"><span data-stu-id="9cec1-341">The previous ownership of this semaphore has ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-342"><span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**ERRO \_ sem \_ limite de usuário \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-342"><span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**ERROR\_SEM\_USER\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-343">106 (0x6A)</span><span class="sxs-lookup"><span data-stu-id="9cec1-343">106 (0x6A)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-344">Insira o disquete para a unidade %1.</span><span class="sxs-lookup"><span data-stu-id="9cec1-344">Insert the diskette for drive %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-345"><span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**ERRO \_ ao \_ alterar disco**</span><span class="sxs-lookup"><span data-stu-id="9cec1-345"><span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**ERROR\_DISK\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-346">107 (0x6B)</span><span class="sxs-lookup"><span data-stu-id="9cec1-346">107 (0x6B)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-347">O programa foi interrompido porque um disquete alternativo não foi inserido.</span><span class="sxs-lookup"><span data-stu-id="9cec1-347">The program stopped because an alternate diskette was not inserted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-348"><span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**unidade de erro \_ \_ bloqueada**</span><span class="sxs-lookup"><span data-stu-id="9cec1-348"><span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**ERROR\_DRIVE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-349">108 (0x6C)</span><span class="sxs-lookup"><span data-stu-id="9cec1-349">108 (0x6C)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-350">O disco está em uso ou está bloqueado por outro processo.</span><span class="sxs-lookup"><span data-stu-id="9cec1-350">The disk is in use or locked by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-351"><span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**ERRO \_ de \_ pipe interrompido**</span><span class="sxs-lookup"><span data-stu-id="9cec1-351"><span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**ERROR\_BROKEN\_PIPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-352">109 (0x6D)</span><span class="sxs-lookup"><span data-stu-id="9cec1-352">109 (0x6D)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-353">O pipe foi encerrado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-353">The pipe has been ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-354"><span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**\_ \_ falha ao abrir erro**</span><span class="sxs-lookup"><span data-stu-id="9cec1-354"><span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**ERROR\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-355">110 (0x6E)</span><span class="sxs-lookup"><span data-stu-id="9cec1-355">110 (0x6E)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-356">O sistema não pode abrir o dispositivo ou o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-356">The system cannot open the device or file specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-357"><span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**\_estouro de buffer de erro \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-357"><span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**ERROR\_BUFFER\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-358">111 (0x6F)</span><span class="sxs-lookup"><span data-stu-id="9cec1-358">111 (0x6F)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-359">O nome do arquivo é muito longo.</span><span class="sxs-lookup"><span data-stu-id="9cec1-359">The file name is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-360"><span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**ERRO de \_ disco \_ cheio**</span><span class="sxs-lookup"><span data-stu-id="9cec1-360"><span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**ERROR\_DISK\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-361">112 (0x70)</span><span class="sxs-lookup"><span data-stu-id="9cec1-361">112 (0x70)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-362">Espaço insuficiente no disco.</span><span class="sxs-lookup"><span data-stu-id="9cec1-362">There is not enough space on the disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-363"><span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**ERRO \_ não \_ há \_ mais \_ identificadores de pesquisa**</span><span class="sxs-lookup"><span data-stu-id="9cec1-363"><span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**ERROR\_NO\_MORE\_SEARCH\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-364">113 (0x71)</span><span class="sxs-lookup"><span data-stu-id="9cec1-364">113 (0x71)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-365">Não há mais identificadores de arquivo internos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9cec1-365">No more internal file identifiers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-366"><span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**ERRO \_ de \_ identificador de destino inválido \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-366"><span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**ERROR\_INVALID\_TARGET\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-367">114 (0x72)</span><span class="sxs-lookup"><span data-stu-id="9cec1-367">114 (0x72)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-368">O identificador de arquivo interno de destino está incorreto.</span><span class="sxs-lookup"><span data-stu-id="9cec1-368">The target internal file identifier is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-369"><span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**Categoria de erro \_ inválida \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-369"><span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**ERROR\_INVALID\_CATEGORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-370">117 (0x75)</span><span class="sxs-lookup"><span data-stu-id="9cec1-370">117 (0x75)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-371">A chamada de IOCTL feita pelo programa de aplicativo não está correta.</span><span class="sxs-lookup"><span data-stu-id="9cec1-371">The IOCTL call made by the application program is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-372"><span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**ERRO \_ ao \_ verificar \_ opção inválida**</span><span class="sxs-lookup"><span data-stu-id="9cec1-372"><span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**ERROR\_INVALID\_VERIFY\_SWITCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-373">118 (0x76)</span><span class="sxs-lookup"><span data-stu-id="9cec1-373">118 (0x76)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-374">O valor do parâmetro de opção verify-on-Write não está correto.</span><span class="sxs-lookup"><span data-stu-id="9cec1-374">The verify-on-write switch parameter value is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-375"><span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**ERRO \_ de \_ nível de driver insatisfatório \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-375"><span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**ERROR\_BAD\_DRIVER\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-376">119 (0x77)</span><span class="sxs-lookup"><span data-stu-id="9cec1-376">119 (0x77)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-377">O sistema não oferece suporte ao comando solicitado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-377">The system does not support the command requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-378"><span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**chamada de erro \_ \_ não \_ implementada**</span><span class="sxs-lookup"><span data-stu-id="9cec1-378"><span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**ERROR\_CALL\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-379">120 (0x78)</span><span class="sxs-lookup"><span data-stu-id="9cec1-379">120 (0x78)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-380">Esta função não tem suporte neste sistema.</span><span class="sxs-lookup"><span data-stu-id="9cec1-380">This function is not supported on this system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-381"><span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**ERRO \_ sem \_ tempo limite**</span><span class="sxs-lookup"><span data-stu-id="9cec1-381"><span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**ERROR\_SEM\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-382">121 (0x79)</span><span class="sxs-lookup"><span data-stu-id="9cec1-382">121 (0x79)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-383">O período de tempo limite de semáforo expirou.</span><span class="sxs-lookup"><span data-stu-id="9cec1-383">The semaphore timeout period has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-384"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERRO \_ de \_ buffer insuficiente**</span><span class="sxs-lookup"><span data-stu-id="9cec1-384"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-385">122 (0x7A)</span><span class="sxs-lookup"><span data-stu-id="9cec1-385">122 (0x7A)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-386">A área de dados passada para uma chamada do sistema é muito pequena.</span><span class="sxs-lookup"><span data-stu-id="9cec1-386">The data area passed to a system call is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-387"><span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**\_nome inválido do erro \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-387"><span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**ERROR\_INVALID\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-388">123 (0x7B)</span><span class="sxs-lookup"><span data-stu-id="9cec1-388">123 (0x7B)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-389">A sintaxe FileName, nome do diretório ou rótulo do volume está incorreta.</span><span class="sxs-lookup"><span data-stu-id="9cec1-389">The filename, directory name, or volume label syntax is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-390"><span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**ERRO \_ de \_ nível inválido**</span><span class="sxs-lookup"><span data-stu-id="9cec1-390"><span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**ERROR\_INVALID\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-391">124 (0x7C)</span><span class="sxs-lookup"><span data-stu-id="9cec1-391">124 (0x7C)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-392">O nível de chamada do sistema não está correto.</span><span class="sxs-lookup"><span data-stu-id="9cec1-392">The system call level is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-393"><span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**ERRO \_ sem \_ rótulo de volume \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-393"><span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**ERROR\_NO\_VOLUME\_LABEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-394">125 (0x7D)</span><span class="sxs-lookup"><span data-stu-id="9cec1-394">125 (0x7D)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-395">O disco não tem nenhum rótulo de volume.</span><span class="sxs-lookup"><span data-stu-id="9cec1-395">The disk has no volume label.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-396"><span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**ERRO \_ mod \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-396"><span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**ERROR\_MOD\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-397">126 (0x7E)</span><span class="sxs-lookup"><span data-stu-id="9cec1-397">126 (0x7E)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-398">O módulo especificado não pôde ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-398">The specified module could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-399"><span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**PROC. de erro \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-399"><span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**ERROR\_PROC\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-400">127 (0x7F)</span><span class="sxs-lookup"><span data-stu-id="9cec1-400">127 (0x7F)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-401">Não foi possível encontrar o procedimento especificado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-401">The specified procedure could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-402"><span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**ERRO ao \_ aguardar \_ nenhum \_ filho**</span><span class="sxs-lookup"><span data-stu-id="9cec1-402"><span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**ERROR\_WAIT\_NO\_CHILDREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-403">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="9cec1-403">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-404">Não há nenhum processo filho a aguardar.</span><span class="sxs-lookup"><span data-stu-id="9cec1-404">There are no child processes to wait for.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-405"><span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**ERRO \_ filho \_ não \_ concluído**</span><span class="sxs-lookup"><span data-stu-id="9cec1-405"><span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**ERROR\_CHILD\_NOT\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-406">129 (0x81)</span><span class="sxs-lookup"><span data-stu-id="9cec1-406">129 (0x81)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-407">O aplicativo %1 não pode ser executado no modo Win32.</span><span class="sxs-lookup"><span data-stu-id="9cec1-407">The %1 application cannot be run in Win32 mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-408"><span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**\_identificador de \_ acesso \_ direto de erro**</span><span class="sxs-lookup"><span data-stu-id="9cec1-408"><span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**ERROR\_DIRECT\_ACCESS\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-409">130 (0x82)</span><span class="sxs-lookup"><span data-stu-id="9cec1-409">130 (0x82)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-410">Tentativa de usar um identificador de arquivo para uma partição de disco aberta para uma operação diferente de e/s de disco bruto.</span><span class="sxs-lookup"><span data-stu-id="9cec1-410">Attempt to use a file handle to an open disk partition for an operation other than raw disk I/O.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-411"><span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**ERRO \_ de \_ busca negativa**</span><span class="sxs-lookup"><span data-stu-id="9cec1-411"><span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**ERROR\_NEGATIVE\_SEEK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-412">131 (0x83)</span><span class="sxs-lookup"><span data-stu-id="9cec1-412">131 (0x83)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-413">Foi feita uma tentativa de mover o ponteiro do arquivo antes do início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="9cec1-413">An attempt was made to move the file pointer before the beginning of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-414"><span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**ERRO ao \_ buscar \_ no \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="9cec1-414"><span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**ERROR\_SEEK\_ON\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-415">132 (0x84)</span><span class="sxs-lookup"><span data-stu-id="9cec1-415">132 (0x84)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-416">O ponteiro do arquivo não pode ser definido no dispositivo ou arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-416">The file pointer cannot be set on the specified device or file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-417"><span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**ERRO \_ é \_ destino de junção \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-417"><span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**ERROR\_IS\_JOIN\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-418">133 (0x85)</span><span class="sxs-lookup"><span data-stu-id="9cec1-418">133 (0x85)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-419">Um comando JOIN ou SUBST não pode ser usado para uma unidade que contém unidades Unidas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9cec1-419">A JOIN or SUBST command cannot be used for a drive that contains previously joined drives.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-420"><span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**ERRO \_ \_ associado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-420"><span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**ERROR\_IS\_JOINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-421">134 (0x86)</span><span class="sxs-lookup"><span data-stu-id="9cec1-421">134 (0x86)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-422">Foi feita uma tentativa de usar um comando JOIN ou SUBST em uma unidade que já foi unida.</span><span class="sxs-lookup"><span data-stu-id="9cec1-422">An attempt was made to use a JOIN or SUBST command on a drive that has already been joined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-423"><span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**ERRO \_ é \_ subst**</span><span class="sxs-lookup"><span data-stu-id="9cec1-423"><span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**ERROR\_IS\_SUBSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-424">135 (0x87)</span><span class="sxs-lookup"><span data-stu-id="9cec1-424">135 (0x87)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-425">Foi feita uma tentativa de usar um comando JOIN ou SUBST em uma unidade que já foi substituída.</span><span class="sxs-lookup"><span data-stu-id="9cec1-425">An attempt was made to use a JOIN or SUBST command on a drive that has already been substituted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-426"><span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**ERRO \_ não \_ ingressado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-426"><span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**ERROR\_NOT\_JOINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-427">136 (0x88)</span><span class="sxs-lookup"><span data-stu-id="9cec1-427">136 (0x88)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-428">O sistema tentou excluir a junção de uma unidade que não está unida.</span><span class="sxs-lookup"><span data-stu-id="9cec1-428">The system tried to delete the JOIN of a drive that is not joined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-429"><span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**ERRO \_ não \_ subst**</span><span class="sxs-lookup"><span data-stu-id="9cec1-429"><span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**ERROR\_NOT\_SUBSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-430">137 (0x89)</span><span class="sxs-lookup"><span data-stu-id="9cec1-430">137 (0x89)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-431">O sistema tentou excluir a substituição de uma unidade que não está substituída.</span><span class="sxs-lookup"><span data-stu-id="9cec1-431">The system tried to delete the substitution of a drive that is not substituted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-432"><span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**ERRO ao \_ ingressar \_ no \_ ingresso**</span><span class="sxs-lookup"><span data-stu-id="9cec1-432"><span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**ERROR\_JOIN\_TO\_JOIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-433">138 (0x8A)</span><span class="sxs-lookup"><span data-stu-id="9cec1-433">138 (0x8A)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-434">O sistema tentou unir uma unidade a um diretório em uma unidade unida.</span><span class="sxs-lookup"><span data-stu-id="9cec1-434">The system tried to join a drive to a directory on a joined drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-435"><span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**ERRO \_ subst \_ para \_ subst**</span><span class="sxs-lookup"><span data-stu-id="9cec1-435"><span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**ERROR\_SUBST\_TO\_SUBST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-436">139 (0x8B)</span><span class="sxs-lookup"><span data-stu-id="9cec1-436">139 (0x8B)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-437">O sistema tentou substituir uma unidade por um diretório em uma unidade substituída.</span><span class="sxs-lookup"><span data-stu-id="9cec1-437">The system tried to substitute a drive to a directory on a substituted drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-438"><span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**ERRO ao \_ ingressar \_ no \_ subst**</span><span class="sxs-lookup"><span data-stu-id="9cec1-438"><span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**ERROR\_JOIN\_TO\_SUBST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-439">140 (0x8C)</span><span class="sxs-lookup"><span data-stu-id="9cec1-439">140 (0x8C)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-440">O sistema tentou unir uma unidade a um diretório em uma unidade substituída.</span><span class="sxs-lookup"><span data-stu-id="9cec1-440">The system tried to join a drive to a directory on a substituted drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-441"><span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**ERRO \_ subst \_ para \_ unir**</span><span class="sxs-lookup"><span data-stu-id="9cec1-441"><span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**ERROR\_SUBST\_TO\_JOIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-442">141 (0x8D)</span><span class="sxs-lookup"><span data-stu-id="9cec1-442">141 (0x8D)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-443">O sistema tentou SUBST uma unidade para um diretório em uma unidade unida.</span><span class="sxs-lookup"><span data-stu-id="9cec1-443">The system tried to SUBST a drive to a directory on a joined drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-444"><span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**unidade de erro \_ ocupada \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-444"><span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**ERROR\_BUSY\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-445">142 (0x8E)</span><span class="sxs-lookup"><span data-stu-id="9cec1-445">142 (0x8E)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-446">O sistema não pode executar um JOIN ou SUBST no momento.</span><span class="sxs-lookup"><span data-stu-id="9cec1-446">The system cannot perform a JOIN or SUBST at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-447"><span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**ERRO na \_ mesma \_ unidade**</span><span class="sxs-lookup"><span data-stu-id="9cec1-447"><span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**ERROR\_SAME\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-448">143 (0x8F)</span><span class="sxs-lookup"><span data-stu-id="9cec1-448">143 (0x8F)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-449">O sistema não pode unir ou substituir uma unidade para ou para um diretório na mesma unidade.</span><span class="sxs-lookup"><span data-stu-id="9cec1-449">The system cannot join or substitute a drive to or for a directory on the same drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-450"><span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**ERRO \_ dir \_ não \_ raiz**</span><span class="sxs-lookup"><span data-stu-id="9cec1-450"><span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**ERROR\_DIR\_NOT\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-451">144 (0x90)</span><span class="sxs-lookup"><span data-stu-id="9cec1-451">144 (0x90)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-452">O diretório não é um subdiretório do diretório raiz.</span><span class="sxs-lookup"><span data-stu-id="9cec1-452">The directory is not a subdirectory of the root directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-453"><span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**ERRO de \_ dir \_ não \_ vazio**</span><span class="sxs-lookup"><span data-stu-id="9cec1-453"><span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**ERROR\_DIR\_NOT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-454">145 (0x91)</span><span class="sxs-lookup"><span data-stu-id="9cec1-454">145 (0x91)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-455">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="9cec1-455">The directory is not empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-456"><span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**ERRO \_ é \_ um \_ caminho subst**</span><span class="sxs-lookup"><span data-stu-id="9cec1-456"><span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**ERROR\_IS\_SUBST\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-457">146 (0x92)</span><span class="sxs-lookup"><span data-stu-id="9cec1-457">146 (0x92)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-458">O caminho especificado está sendo usado em um substituto.</span><span class="sxs-lookup"><span data-stu-id="9cec1-458">The path specified is being used in a substitute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-459"><span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**ERRO \_ é \_ um \_ caminho de junção**</span><span class="sxs-lookup"><span data-stu-id="9cec1-459"><span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**ERROR\_IS\_JOIN\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-460">147 (0x93)</span><span class="sxs-lookup"><span data-stu-id="9cec1-460">147 (0x93)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-461">Não há recursos suficientes disponíveis para processar este comando.</span><span class="sxs-lookup"><span data-stu-id="9cec1-461">Not enough resources are available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-462"><span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**caminho de erro \_ \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-462"><span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**ERROR\_PATH\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-463">148 (0x94)</span><span class="sxs-lookup"><span data-stu-id="9cec1-463">148 (0x94)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-464">O caminho especificado não pode ser usado neste momento.</span><span class="sxs-lookup"><span data-stu-id="9cec1-464">The path specified cannot be used at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-465"><span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**ERRO \_ é \_ \_ destino subst**</span><span class="sxs-lookup"><span data-stu-id="9cec1-465"><span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**ERROR\_IS\_SUBST\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-466">149 (0x95)</span><span class="sxs-lookup"><span data-stu-id="9cec1-466">149 (0x95)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-467">Foi feita uma tentativa de unir ou substituir uma unidade para a qual um diretório na unidade é o destino de um substituto anterior.</span><span class="sxs-lookup"><span data-stu-id="9cec1-467">An attempt was made to join or substitute a drive for which a directory on the drive is the target of a previous substitute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-468"><span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**\_rastreamento do sistema de erro \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-468"><span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**ERROR\_SYSTEM\_TRACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-469">150 (0x96)</span><span class="sxs-lookup"><span data-stu-id="9cec1-469">150 (0x96)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-470">As informações de rastreamento do sistema não foram especificadas no arquivo de CONFIG.SYS, ou o rastreamento não é permitido.</span><span class="sxs-lookup"><span data-stu-id="9cec1-470">System trace information was not specified in your CONFIG.SYS file, or tracing is disallowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-471"><span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**contagem de eventos de erro \_ inválido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-471"><span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**ERROR\_INVALID\_EVENT\_COUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-472">151 (0x97)</span><span class="sxs-lookup"><span data-stu-id="9cec1-472">151 (0x97)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-473">O número de eventos de semáforo especificados para DosMuxSemWait não está correto.</span><span class="sxs-lookup"><span data-stu-id="9cec1-473">The number of specified semaphore events for DosMuxSemWait is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-474"><span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**ERRO em excesso de \_ \_ \_ MUXWAITERS**</span><span class="sxs-lookup"><span data-stu-id="9cec1-474"><span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**ERROR\_TOO\_MANY\_MUXWAITERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-475">152 (0x98)</span><span class="sxs-lookup"><span data-stu-id="9cec1-475">152 (0x98)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-476">DosMuxSemWait não foi executado; muitos semáforos já estão definidos.</span><span class="sxs-lookup"><span data-stu-id="9cec1-476">DosMuxSemWait did not execute; too many semaphores are already set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-477"><span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**ERRO \_ de \_ formato de lista inválido \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-477"><span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**ERROR\_INVALID\_LIST\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-478">153 (0x99)</span><span class="sxs-lookup"><span data-stu-id="9cec1-478">153 (0x99)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-479">A lista DosMuxSemWait não está correta.</span><span class="sxs-lookup"><span data-stu-id="9cec1-479">The DosMuxSemWait list is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-480"><span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**rótulo de erro \_ \_ muito \_ longo**</span><span class="sxs-lookup"><span data-stu-id="9cec1-480"><span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**ERROR\_LABEL\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-481">154 (0x9A)</span><span class="sxs-lookup"><span data-stu-id="9cec1-481">154 (0x9A)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-482">O rótulo do volume inserido excede o limite de caracteres do rótulo do sistema de arquivos de destino.</span><span class="sxs-lookup"><span data-stu-id="9cec1-482">The volume label you entered exceeds the label character limit of the target file system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-483"><span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**ERRO em excesso de \_ \_ \_ TCBS**</span><span class="sxs-lookup"><span data-stu-id="9cec1-483"><span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**ERROR\_TOO\_MANY\_TCBS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-484">155 (0x9B)</span><span class="sxs-lookup"><span data-stu-id="9cec1-484">155 (0x9B)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-485">Não é possível criar outro thread.</span><span class="sxs-lookup"><span data-stu-id="9cec1-485">Cannot create another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-486"><span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**sinal de erro \_ \_ recusado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-486"><span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**ERROR\_SIGNAL\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-487">156 (0x9C)</span><span class="sxs-lookup"><span data-stu-id="9cec1-487">156 (0x9C)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-488">O processo de destinatário recusou o sinal.</span><span class="sxs-lookup"><span data-stu-id="9cec1-488">The recipient process has refused the signal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-489"><span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**ERRO \_ Descartado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-489"><span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**ERROR\_DISCARDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-490">157 (0x9D)</span><span class="sxs-lookup"><span data-stu-id="9cec1-490">157 (0x9D)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-491">O segmento já foi descartado e não pode ser bloqueado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-491">The segment is already discarded and cannot be locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-492"><span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**ERRO \_ não \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-492"><span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**ERROR\_NOT\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-493">158 (0x9E)</span><span class="sxs-lookup"><span data-stu-id="9cec1-493">158 (0x9E)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-494">O segmento já está desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-494">The segment is already unlocked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-495"><span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**ERRO \_ de \_ THREADID de endereço inadequado \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-495"><span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**ERROR\_BAD\_THREADID\_ADDR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-496">159 (0x9F)</span><span class="sxs-lookup"><span data-stu-id="9cec1-496">159 (0x9F)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-497">O endereço da ID do thread não está correto.</span><span class="sxs-lookup"><span data-stu-id="9cec1-497">The address for the thread ID is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-498"><span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**ERROS de \_ argumentos inválidos \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-498"><span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**ERROR\_BAD\_ARGUMENTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-499">160 (0xA0)</span><span class="sxs-lookup"><span data-stu-id="9cec1-499">160 (0xA0)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-500">Um ou mais argumentos não estão corretos.</span><span class="sxs-lookup"><span data-stu-id="9cec1-500">One or more arguments are not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-501"><span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**ERRO \_ nome de caminho insatisfatório \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-501"><span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**ERROR\_BAD\_PATHNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-502">161 (0xA1)</span><span class="sxs-lookup"><span data-stu-id="9cec1-502">161 (0xA1)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-503">O caminho especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="9cec1-503">The specified path is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-504"><span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**sinal de erro \_ \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="9cec1-504"><span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**ERROR\_SIGNAL\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-505">162 (0xA2)</span><span class="sxs-lookup"><span data-stu-id="9cec1-505">162 (0xA2)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-506">Já existe um sinal pendente.</span><span class="sxs-lookup"><span data-stu-id="9cec1-506">A signal is already pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-507"><span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**ERRO \_ Max \_ THRDS \_ atingido**</span><span class="sxs-lookup"><span data-stu-id="9cec1-507"><span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**ERROR\_MAX\_THRDS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-508">164 (0xA4)</span><span class="sxs-lookup"><span data-stu-id="9cec1-508">164 (0xA4)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-509">Não é possível criar mais threads no sistema.</span><span class="sxs-lookup"><span data-stu-id="9cec1-509">No more threads can be created in the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-510"><span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**\_falha no bloqueio de erro \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-510"><span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**ERROR\_LOCK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-511">167 (0xA7)</span><span class="sxs-lookup"><span data-stu-id="9cec1-511">167 (0xA7)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-512">Não é possível bloquear uma região de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="9cec1-512">Unable to lock a region of a file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-513"><span id="ERROR_BUSY"></span><span id="error_busy"></span>**ERRO \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-513"><span id="ERROR_BUSY"></span><span id="error_busy"></span>**ERROR\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-514">170 (0xAA)</span><span class="sxs-lookup"><span data-stu-id="9cec1-514">170 (0xAA)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-515">O recurso solicitado está em uso.</span><span class="sxs-lookup"><span data-stu-id="9cec1-515">The requested resource is in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-516"><span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**\_ \_ suporte ao dispositivo \_ de erro em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="9cec1-516"><span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**ERROR\_DEVICE\_SUPPORT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-517">171 (0xAB)</span><span class="sxs-lookup"><span data-stu-id="9cec1-517">171 (0xAB)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-518">A detecção de suporte de comando do dispositivo está em andamento.</span><span class="sxs-lookup"><span data-stu-id="9cec1-518">Device's command support detection is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-519"><span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**ERRO de \_ cancelamento de \_ violação**</span><span class="sxs-lookup"><span data-stu-id="9cec1-519"><span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**ERROR\_CANCEL\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-520">173 (0xAD)</span><span class="sxs-lookup"><span data-stu-id="9cec1-520">173 (0xAD)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-521">Uma solicitação de bloqueio não estava pendente para a região de cancelamento fornecida.</span><span class="sxs-lookup"><span data-stu-id="9cec1-521">A lock request was not outstanding for the supplied cancel region.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-522"><span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**ERRO \_ de \_ bloqueios atômicos \_ sem \_ suporte**</span><span class="sxs-lookup"><span data-stu-id="9cec1-522"><span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**ERROR\_ATOMIC\_LOCKS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-523">174 (0xAE)</span><span class="sxs-lookup"><span data-stu-id="9cec1-523">174 (0xAE)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-524">O sistema de arquivos não dá suporte a alterações atômicas para o tipo de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="9cec1-524">The file system does not support atomic changes to the lock type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-525"><span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**\_número de \_ segmento \_ inválido do erro**</span><span class="sxs-lookup"><span data-stu-id="9cec1-525"><span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**ERROR\_INVALID\_SEGMENT\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-526">180 (0xB4)</span><span class="sxs-lookup"><span data-stu-id="9cec1-526">180 (0xB4)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-527">O sistema detectou um número de segmento que não estava correto.</span><span class="sxs-lookup"><span data-stu-id="9cec1-527">The system detected a segment number that was not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-528"><span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**ERRO \_ \_ ORDINAL inválido**</span><span class="sxs-lookup"><span data-stu-id="9cec1-528"><span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**ERROR\_INVALID\_ORDINAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-529">182 (0xB6)</span><span class="sxs-lookup"><span data-stu-id="9cec1-529">182 (0xB6)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-530">O sistema operacional não pode executar %1.</span><span class="sxs-lookup"><span data-stu-id="9cec1-530">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-531"><span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**o erro \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="9cec1-531"><span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**ERROR\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-532">183 (0xB7)</span><span class="sxs-lookup"><span data-stu-id="9cec1-532">183 (0xB7)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-533">Não é possível criar um arquivo quando ele já existe.</span><span class="sxs-lookup"><span data-stu-id="9cec1-533">Cannot create a file when that file already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-534"><span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**ERRO \_ \_ número de sinalizador inválido \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-534"><span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**ERROR\_INVALID\_FLAG\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-535">186 (0xBA)</span><span class="sxs-lookup"><span data-stu-id="9cec1-535">186 (0xBA)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-536">O sinalizador passado não está correto.</span><span class="sxs-lookup"><span data-stu-id="9cec1-536">The flag passed is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-537"><span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**ERRO \_ sem \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-537"><span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**ERROR\_SEM\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-538">187 (0xBB)</span><span class="sxs-lookup"><span data-stu-id="9cec1-538">187 (0xBB)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-539">O nome do semáforo do sistema especificado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-539">The specified system semaphore name was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-540"><span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**erro \_ inválido ao \_ Iniciar \_ CODESEG**</span><span class="sxs-lookup"><span data-stu-id="9cec1-540"><span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**ERROR\_INVALID\_STARTING\_CODESEG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-541">188 (0xBC)</span><span class="sxs-lookup"><span data-stu-id="9cec1-541">188 (0xBC)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-542">O sistema operacional não pode executar %1.</span><span class="sxs-lookup"><span data-stu-id="9cec1-542">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-543"><span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**ERRO \_ \_ STACKSEG inválido**</span><span class="sxs-lookup"><span data-stu-id="9cec1-543"><span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**ERROR\_INVALID\_STACKSEG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-544">189 (0xBD)</span><span class="sxs-lookup"><span data-stu-id="9cec1-544">189 (0xBD)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-545">O sistema operacional não pode executar %1.</span><span class="sxs-lookup"><span data-stu-id="9cec1-545">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-546"><span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**ERRO \_ de \_ ModuleType inválido**</span><span class="sxs-lookup"><span data-stu-id="9cec1-546"><span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**ERROR\_INVALID\_MODULETYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-547">190 (0xBE)</span><span class="sxs-lookup"><span data-stu-id="9cec1-547">190 (0xBE)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-548">O sistema operacional não pode executar %1.</span><span class="sxs-lookup"><span data-stu-id="9cec1-548">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-549"><span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**ERRO \_ de \_ assinatura exe inválida \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-549"><span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**ERROR\_INVALID\_EXE\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-550">191 (0xBF)</span><span class="sxs-lookup"><span data-stu-id="9cec1-550">191 (0xBF)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-551">Não é possível executar %1 no modo Win32.</span><span class="sxs-lookup"><span data-stu-id="9cec1-551">Cannot run %1 in Win32 mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-552"><span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**ERRO \_ exe \_ marcado como \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="9cec1-552"><span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**ERROR\_EXE\_MARKED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-553">192 (0xC0)</span><span class="sxs-lookup"><span data-stu-id="9cec1-553">192 (0xC0)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-554">O sistema operacional não pode executar %1.</span><span class="sxs-lookup"><span data-stu-id="9cec1-554">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-555"><span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**ERRO \_ de \_ formato exe insatisfatório \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-555"><span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**ERROR\_BAD\_EXE\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-556">193 (0xC1)</span><span class="sxs-lookup"><span data-stu-id="9cec1-556">193 (0xC1)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-557">%1 não é um aplicativo Win32 válido.</span><span class="sxs-lookup"><span data-stu-id="9cec1-557">%1 is not a valid Win32 application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-558"><span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**\_Dados iterados de erro \_ \_ excedem \_ 64K**</span><span class="sxs-lookup"><span data-stu-id="9cec1-558"><span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**ERROR\_ITERATED\_DATA\_EXCEEDS\_64k**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-559">194 (0xC2)</span><span class="sxs-lookup"><span data-stu-id="9cec1-559">194 (0xC2)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-560">O sistema operacional não pode executar %1.</span><span class="sxs-lookup"><span data-stu-id="9cec1-560">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-561"><span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**ERRO \_ \_ MINALLOCSIZE inválido**</span><span class="sxs-lookup"><span data-stu-id="9cec1-561"><span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**ERROR\_INVALID\_MINALLOCSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-562">195 (0xC3)</span><span class="sxs-lookup"><span data-stu-id="9cec1-562">195 (0xC3)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-563">O sistema operacional não pode executar %1.</span><span class="sxs-lookup"><span data-stu-id="9cec1-563">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-564"><span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**ERRO \_ DYNLINK \_ de \_ \_ anel inválido**</span><span class="sxs-lookup"><span data-stu-id="9cec1-564"><span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**ERROR\_DYNLINK\_FROM\_INVALID\_RING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-565">196 (0xC4)</span><span class="sxs-lookup"><span data-stu-id="9cec1-565">196 (0xC4)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-566">O sistema operacional não pode executar este programa de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9cec1-566">The operating system cannot run this application program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-567"><span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**ERRO \_ IOPL \_ não \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-567"><span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**ERROR\_IOPL\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-568">197 (0xC5)</span><span class="sxs-lookup"><span data-stu-id="9cec1-568">197 (0xC5)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-569">O sistema operacional não está configurado atualmente para executar este aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9cec1-569">The operating system is not presently configured to run this application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-570"><span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**ERRO \_ \_ SEGDPL inválido**</span><span class="sxs-lookup"><span data-stu-id="9cec1-570"><span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**ERROR\_INVALID\_SEGDPL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-571">198 (0xC6)</span><span class="sxs-lookup"><span data-stu-id="9cec1-571">198 (0xC6)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-572">O sistema operacional não pode executar %1.</span><span class="sxs-lookup"><span data-stu-id="9cec1-572">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-573"><span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**O erro \_ AUTODATASEG \_ excede \_ 64K**</span><span class="sxs-lookup"><span data-stu-id="9cec1-573"><span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**ERROR\_AUTODATASEG\_EXCEEDS\_64k**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-574">199 (0xC7)</span><span class="sxs-lookup"><span data-stu-id="9cec1-574">199 (0xC7)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-575">O sistema operacional não pode executar este programa de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9cec1-575">The operating system cannot run this application program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-576"><span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**O erro \_ RING2SEG \_ deve \_ ser \_ móvel**</span><span class="sxs-lookup"><span data-stu-id="9cec1-576"><span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**ERROR\_RING2SEG\_MUST\_BE\_MOVABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-577">200 (0xC8)</span><span class="sxs-lookup"><span data-stu-id="9cec1-577">200 (0xC8)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-578">O segmento de código não pode ser maior ou igual a 64K.</span><span class="sxs-lookup"><span data-stu-id="9cec1-578">The code segment cannot be greater than or equal to 64K.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-579"><span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**ERRO \_ realocação \_ Chain \_ XEEDS \_ SEGLIM**</span><span class="sxs-lookup"><span data-stu-id="9cec1-579"><span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**ERROR\_RELOC\_CHAIN\_XEEDS\_SEGLIM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-580">201 (0xC9)</span><span class="sxs-lookup"><span data-stu-id="9cec1-580">201 (0xC9)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-581">O sistema operacional não pode executar %1.</span><span class="sxs-lookup"><span data-stu-id="9cec1-581">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-582"><span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**ERRO \_ INFLOOP \_ na \_ cadeia de realocação \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-582"><span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**ERROR\_INFLOOP\_IN\_RELOC\_CHAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-583">202 (0xCA)</span><span class="sxs-lookup"><span data-stu-id="9cec1-583">202 (0xCA)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-584">O sistema operacional não pode executar %1.</span><span class="sxs-lookup"><span data-stu-id="9cec1-584">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-585"><span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**ERRO \_ ENVVAR \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-585"><span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**ERROR\_ENVVAR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-586">203 (0xCB)</span><span class="sxs-lookup"><span data-stu-id="9cec1-586">203 (0xCB)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-587">O sistema não pôde encontrar a opção de ambiente que foi inserida.</span><span class="sxs-lookup"><span data-stu-id="9cec1-587">The system could not find the environment option that was entered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-588"><span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**ERRO \_ nenhum \_ sinal \_ enviado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-588"><span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**ERROR\_NO\_SIGNAL\_SENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-589">205 (0xCD)</span><span class="sxs-lookup"><span data-stu-id="9cec1-589">205 (0xCD)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-590">Nenhum processo na subárvore de comandos tem um manipulador de sinais.</span><span class="sxs-lookup"><span data-stu-id="9cec1-590">No process in the command subtree has a signal handler.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-591"><span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**ERRO \_ de \_ intervalo de EXCED de nome \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-591"><span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**ERROR\_FILENAME\_EXCED\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-592">206 (0xCE)</span><span class="sxs-lookup"><span data-stu-id="9cec1-592">206 (0xCE)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-593">O nome do arquivo ou a extensão é muito longa.</span><span class="sxs-lookup"><span data-stu-id="9cec1-593">The filename or extension is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-594"><span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**ERRO \_ \_ de pilha RING2 \_ em \_ uso**</span><span class="sxs-lookup"><span data-stu-id="9cec1-594"><span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**ERROR\_RING2\_STACK\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-595">207 (0xCF)</span><span class="sxs-lookup"><span data-stu-id="9cec1-595">207 (0xCF)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-596">A pilha de anéis 2 está em uso.</span><span class="sxs-lookup"><span data-stu-id="9cec1-596">The ring 2 stack is in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-597"><span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**metaexpansão de erro \_ \_ \_ muito \_ longa**</span><span class="sxs-lookup"><span data-stu-id="9cec1-597"><span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**ERROR\_META\_EXPANSION\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-598">208 (0xD0)</span><span class="sxs-lookup"><span data-stu-id="9cec1-598">208 (0xD0)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-599">Os caracteres de nome de arquivo global, \* ou?, foram inseridos incorretamente ou foram especificados muitos caracteres de nome de arquivo global.</span><span class="sxs-lookup"><span data-stu-id="9cec1-599">The global filename characters, \* or ?, are entered incorrectly or too many global filename characters are specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-600"><span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**\_número de \_ sinal \_ inválido do erro**</span><span class="sxs-lookup"><span data-stu-id="9cec1-600"><span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**ERROR\_INVALID\_SIGNAL\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-601">209 (0xD1)</span><span class="sxs-lookup"><span data-stu-id="9cec1-601">209 (0xD1)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-602">O sinal que está sendo Postado não está correto.</span><span class="sxs-lookup"><span data-stu-id="9cec1-602">The signal being posted is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-603"><span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**ERRO de \_ thread \_ 1 \_ inativo**</span><span class="sxs-lookup"><span data-stu-id="9cec1-603"><span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**ERROR\_THREAD\_1\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-604">210 (0xD2)</span><span class="sxs-lookup"><span data-stu-id="9cec1-604">210 (0xD2)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-605">Não é possível definir o manipulador de sinais.</span><span class="sxs-lookup"><span data-stu-id="9cec1-605">The signal handler cannot be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-606"><span id="ERROR_LOCKED"></span><span id="error_locked"></span>**ERRO \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-606"><span id="ERROR_LOCKED"></span><span id="error_locked"></span>**ERROR\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-607">212 (0xD4)</span><span class="sxs-lookup"><span data-stu-id="9cec1-607">212 (0xD4)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-608">O segmento está bloqueado e não pode ser realocado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-608">The segment is locked and cannot be reallocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-609"><span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**ERRO \_ de \_ muitos \_ módulos**</span><span class="sxs-lookup"><span data-stu-id="9cec1-609"><span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**ERROR\_TOO\_MANY\_MODULES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-610">214 (0xD6)</span><span class="sxs-lookup"><span data-stu-id="9cec1-610">214 (0xD6)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-611">Muitos módulos de vínculo dinâmico estão anexados a este programa ou módulo de vínculo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="9cec1-611">Too many dynamic-link modules are attached to this program or dynamic-link module.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-612"><span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**\_aninhamento de erro \_ não \_ permitido**</span><span class="sxs-lookup"><span data-stu-id="9cec1-612"><span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**ERROR\_NESTING\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-613">215 (0xD7)</span><span class="sxs-lookup"><span data-stu-id="9cec1-613">215 (0xD7)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-614">Não é possível aninhar chamadas para LoadModule.</span><span class="sxs-lookup"><span data-stu-id="9cec1-614">Cannot nest calls to LoadModule.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-615"><span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**ERRO \_ de \_ tipo de computador exe \_ \_ incompatível**</span><span class="sxs-lookup"><span data-stu-id="9cec1-615"><span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**ERROR\_EXE\_MACHINE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-616">216 (0xD8)</span><span class="sxs-lookup"><span data-stu-id="9cec1-616">216 (0xD8)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-617">Esta versão do %1 não é compatível com a versão do Windows que você está executando.</span><span class="sxs-lookup"><span data-stu-id="9cec1-617">This version of %1 is not compatible with the version of Windows you're running.</span></span> <span data-ttu-id="9cec1-618">Verifique as informações do sistema do seu computador e entre em contato com o fornecedor do software.</span><span class="sxs-lookup"><span data-stu-id="9cec1-618">Check your computer's system information and then contact the software publisher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-619"><span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**ERRO \_ exe \_ não \_ pode \_ Modificar \_ binário assinado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-619"><span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**ERROR\_EXE\_CANNOT\_MODIFY\_SIGNED\_BINARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-620">217 (0xD9)</span><span class="sxs-lookup"><span data-stu-id="9cec1-620">217 (0xD9)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-621">O arquivo de imagem %1 está assinado; não é possível modificá-lo.</span><span class="sxs-lookup"><span data-stu-id="9cec1-621">The image file %1 is signed, unable to modify.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-622"><span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**ERRO \_ exe \_ não \_ pode \_ Modificar \_ binário assinado forte \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-622"><span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**ERROR\_EXE\_CANNOT\_MODIFY\_STRONG\_SIGNED\_BINARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-623">218 (0xDA)</span><span class="sxs-lookup"><span data-stu-id="9cec1-623">218 (0xDA)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-624">O arquivo de imagem %1 tem uma assinatura forte, não é possível modificar.</span><span class="sxs-lookup"><span data-stu-id="9cec1-624">The image file %1 is strong signed, unable to modify.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-625"><span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**arquivo de erro \_ \_ com check- \_ out**</span><span class="sxs-lookup"><span data-stu-id="9cec1-625"><span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**ERROR\_FILE\_CHECKED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-626">220 (0xDC)</span><span class="sxs-lookup"><span data-stu-id="9cec1-626">220 (0xDC)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-627">O check-out deste arquivo foi feito ou bloqueado para edição por outro usuário.</span><span class="sxs-lookup"><span data-stu-id="9cec1-627">This file is checked out or locked for editing by another user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-628"><span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**\_check-out de erro \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="9cec1-628"><span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**ERROR\_CHECKOUT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-629">221 (0xDD)</span><span class="sxs-lookup"><span data-stu-id="9cec1-629">221 (0xDD)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-630">É necessário fazer check-out do arquivo antes de salvar as alterações.</span><span class="sxs-lookup"><span data-stu-id="9cec1-630">The file must be checked out before saving changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-631"><span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**ERRO \_ de \_ tipo de arquivo insatisfatório \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-631"><span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**ERROR\_BAD\_FILE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-632">222 (0xDE)</span><span class="sxs-lookup"><span data-stu-id="9cec1-632">222 (0xDE)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-633">O tipo de arquivo que está sendo salvo ou recuperado foi bloqueado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-633">The file type being saved or retrieved has been blocked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-634"><span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**arquivo de erro \_ \_ muito \_ grande**</span><span class="sxs-lookup"><span data-stu-id="9cec1-634"><span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**ERROR\_FILE\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-635">223 (0xDF)</span><span class="sxs-lookup"><span data-stu-id="9cec1-635">223 (0xDF)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-636">O tamanho do arquivo excede o limite permitido e não pode ser salvo.</span><span class="sxs-lookup"><span data-stu-id="9cec1-636">The file size exceeds the limit allowed and cannot be saved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-637"><span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**autenticação de formulários de erro \_ \_ \_ necessária**</span><span class="sxs-lookup"><span data-stu-id="9cec1-637"><span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**ERROR\_FORMS\_AUTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-638">224 (0xE0)</span><span class="sxs-lookup"><span data-stu-id="9cec1-638">224 (0xE0)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-639">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-639">Access Denied.</span></span> <span data-ttu-id="9cec1-640">Antes de abrir os arquivos neste local, você deve primeiro adicionar o site à sua lista de sites confiáveis, navegar até o site e selecionar a opção para fazer logon automaticamente.</span><span class="sxs-lookup"><span data-stu-id="9cec1-640">Before opening files in this location, you must first add the web site to your trusted sites list, browse to the web site, and select the option to login automatically.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-641"><span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**vírus de erro \_ \_ infectado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-641"><span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**ERROR\_VIRUS\_INFECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-642">225 (0xE1)</span><span class="sxs-lookup"><span data-stu-id="9cec1-642">225 (0xE1)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-643">A operação não foi concluída com êxito porque o arquivo contém um vírus ou software potencialmente indesejado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-643">Operation did not complete successfully because the file contains a virus or potentially unwanted software.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-644"><span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**vírus de erro \_ \_ excluído**</span><span class="sxs-lookup"><span data-stu-id="9cec1-644"><span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**ERROR\_VIRUS\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-645">226 (0xE2)</span><span class="sxs-lookup"><span data-stu-id="9cec1-645">226 (0xE2)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-646">Esse arquivo contém um vírus ou software potencialmente indesejado e não pode ser aberto.</span><span class="sxs-lookup"><span data-stu-id="9cec1-646">This file contains a virus or potentially unwanted software and cannot be opened.</span></span> <span data-ttu-id="9cec1-647">Devido à natureza deste vírus ou software potencialmente indesejado, o arquivo foi removido deste local.</span><span class="sxs-lookup"><span data-stu-id="9cec1-647">Due to the nature of this virus or potentially unwanted software, the file has been removed from this location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-648"><span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**\_local do pipe de erros \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-648"><span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**ERROR\_PIPE\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-649">229 (0xE5)</span><span class="sxs-lookup"><span data-stu-id="9cec1-649">229 (0xE5)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-650">O pipe é local.</span><span class="sxs-lookup"><span data-stu-id="9cec1-650">The pipe is local.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-651"><span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**ERRO \_ de \_ pipe insatisfatório**</span><span class="sxs-lookup"><span data-stu-id="9cec1-651"><span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**ERROR\_BAD\_PIPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-652">230 (0xE6)</span><span class="sxs-lookup"><span data-stu-id="9cec1-652">230 (0xE6)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-653">O estado do pipe é inválido.</span><span class="sxs-lookup"><span data-stu-id="9cec1-653">The pipe state is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-654"><span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**PIPE de erro \_ \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-654"><span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**ERROR\_PIPE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-655">231 (0xE7)</span><span class="sxs-lookup"><span data-stu-id="9cec1-655">231 (0xE7)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-656">Todas as instâncias de pipe estão ocupadas.</span><span class="sxs-lookup"><span data-stu-id="9cec1-656">All pipe instances are busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-657"><span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**ERRO \_ sem \_ dados**</span><span class="sxs-lookup"><span data-stu-id="9cec1-657"><span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**ERROR\_NO\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-658">232 (0xE8)</span><span class="sxs-lookup"><span data-stu-id="9cec1-658">232 (0xE8)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-659">O pipe está sendo fechado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-659">The pipe is being closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-660"><span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**PIPE de erro \_ \_ não \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-660"><span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**ERROR\_PIPE\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-661">233 (0xE9)</span><span class="sxs-lookup"><span data-stu-id="9cec1-661">233 (0xE9)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-662">Nenhum processo está na outra extremidade do pipe.</span><span class="sxs-lookup"><span data-stu-id="9cec1-662">No process is on the other end of the pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-663"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERRO de \_ mais \_ dados**</span><span class="sxs-lookup"><span data-stu-id="9cec1-663"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERROR\_MORE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-664">234 (0xEA)</span><span class="sxs-lookup"><span data-stu-id="9cec1-664">234 (0xEA)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-665">Mais dados disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9cec1-665">More data is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-666"><span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**ERRO \_ vc \_ desconectado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-666"><span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**ERROR\_VC\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-667">240 (0xF0)</span><span class="sxs-lookup"><span data-stu-id="9cec1-667">240 (0xF0)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-668">A sessão foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="9cec1-668">The session was canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-669"><span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**ERRO \_ \_ nome ea \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="9cec1-669"><span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**ERROR\_INVALID\_EA\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-670">254 (0xFE)</span><span class="sxs-lookup"><span data-stu-id="9cec1-670">254 (0xFE)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-671">O nome do atributo estendido especificado era inválido.</span><span class="sxs-lookup"><span data-stu-id="9cec1-671">The specified extended attribute name was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-672"><span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**ERRO \_ de \_ lista de ea \_ inconsistente**</span><span class="sxs-lookup"><span data-stu-id="9cec1-672"><span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**ERROR\_EA\_LIST\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-673">255 (0xFF)</span><span class="sxs-lookup"><span data-stu-id="9cec1-673">255 (0xFF)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-674">Os atributos estendidos são inconsistentes.</span><span class="sxs-lookup"><span data-stu-id="9cec1-674">The extended attributes are inconsistent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-675"><span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**\_tempo limite de espera**</span><span class="sxs-lookup"><span data-stu-id="9cec1-675"><span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**WAIT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-676">258 (0x102)</span><span class="sxs-lookup"><span data-stu-id="9cec1-676">258 (0x102)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-677">A operação de espera expirou.</span><span class="sxs-lookup"><span data-stu-id="9cec1-677">The wait operation timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-678"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERRO \_ não há \_ mais \_ itens**</span><span class="sxs-lookup"><span data-stu-id="9cec1-678"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERROR\_NO\_MORE\_ITEMS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-679">259 (0x103)</span><span class="sxs-lookup"><span data-stu-id="9cec1-679">259 (0x103)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-680">Não existem mais dados disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9cec1-680">No more data is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-681"><span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**ERRO \_ não é possível \_ copiar**</span><span class="sxs-lookup"><span data-stu-id="9cec1-681"><span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**ERROR\_CANNOT\_COPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-682">266 (0x10A)</span><span class="sxs-lookup"><span data-stu-id="9cec1-682">266 (0x10A)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-683">As funções de cópia não podem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="9cec1-683">The copy functions cannot be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-684"><span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**diretório de erros \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-684"><span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**ERROR\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-685">267 (0x10B)</span><span class="sxs-lookup"><span data-stu-id="9cec1-685">267 (0x10B)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-686">O nome do diretório é inválido.</span><span class="sxs-lookup"><span data-stu-id="9cec1-686">The directory name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-687"><span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**ERRO \_ EAS \_ \_ desencaixado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-687"><span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**ERROR\_EAS\_DIDNT\_FIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-688">275 (0x113)</span><span class="sxs-lookup"><span data-stu-id="9cec1-688">275 (0x113)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-689">Os atributos estendidos não couberam no buffer.</span><span class="sxs-lookup"><span data-stu-id="9cec1-689">The extended attributes did not fit in the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-690"><span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**ERRO \_ de \_ arquivo ea \_ corrompido**</span><span class="sxs-lookup"><span data-stu-id="9cec1-690"><span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**ERROR\_EA\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-691">276 (0x114)</span><span class="sxs-lookup"><span data-stu-id="9cec1-691">276 (0x114)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-692">O arquivo de atributo estendido no sistema de arquivos montado está corrompido.</span><span class="sxs-lookup"><span data-stu-id="9cec1-692">The extended attribute file on the mounted file system is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-693"><span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**ERRO \_ de \_ tabela de ea \_ cheia**</span><span class="sxs-lookup"><span data-stu-id="9cec1-693"><span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**ERROR\_EA\_TABLE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-694">277 (0x115)</span><span class="sxs-lookup"><span data-stu-id="9cec1-694">277 (0x115)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-695">O arquivo da tabela de atributos estendidos está cheio.</span><span class="sxs-lookup"><span data-stu-id="9cec1-695">The extended attribute table file is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-696"><span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**ERRO \_ de \_ identificador ea inválido \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-696"><span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**ERROR\_INVALID\_EA\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-697">278 (0x116)</span><span class="sxs-lookup"><span data-stu-id="9cec1-697">278 (0x116)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-698">O identificador de atributo estendido especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="9cec1-698">The specified extended attribute handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-699"><span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**ERRO \_ EAS \_ sem \_ suporte**</span><span class="sxs-lookup"><span data-stu-id="9cec1-699"><span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**ERROR\_EAS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-700">282 (0x11A)</span><span class="sxs-lookup"><span data-stu-id="9cec1-700">282 (0x11A)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-701">O sistema de arquivos montado não oferece suporte a atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="9cec1-701">The mounted file system does not support extended attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-702"><span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**ERRO \_ não \_ proprietário**</span><span class="sxs-lookup"><span data-stu-id="9cec1-702"><span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**ERROR\_NOT\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-703">288 (0x120)</span><span class="sxs-lookup"><span data-stu-id="9cec1-703">288 (0x120)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-704">Tentativa de liberar mutex não pertencente ao chamador.</span><span class="sxs-lookup"><span data-stu-id="9cec1-704">Attempt to release mutex not owned by caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-705"><span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**ERRO \_ em \_ muitas \_ postagens**</span><span class="sxs-lookup"><span data-stu-id="9cec1-705"><span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**ERROR\_TOO\_MANY\_POSTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-706">298 (0x12A)</span><span class="sxs-lookup"><span data-stu-id="9cec1-706">298 (0x12A)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-707">Foram feitas muitas postagens em um semáforo.</span><span class="sxs-lookup"><span data-stu-id="9cec1-707">Too many posts were made to a semaphore.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-708"><span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**ERRO \_ de \_ cópia parcial**</span><span class="sxs-lookup"><span data-stu-id="9cec1-708"><span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**ERROR\_PARTIAL\_COPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-709">299 (0x12B)</span><span class="sxs-lookup"><span data-stu-id="9cec1-709">299 (0x12B)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-710">Somente parte de uma solicitação de ReadProcessMemory ou WriteProcessMemory foi concluída.</span><span class="sxs-lookup"><span data-stu-id="9cec1-710">Only part of a ReadProcessMemory or WriteProcessMemory request was completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-711"><span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**ERRO \_ oplock \_ não \_ concedido**</span><span class="sxs-lookup"><span data-stu-id="9cec1-711"><span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**ERROR\_OPLOCK\_NOT\_GRANTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-712">300 (0x12C)</span><span class="sxs-lookup"><span data-stu-id="9cec1-712">300 (0x12C)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-713">A solicitação oplock foi negada.</span><span class="sxs-lookup"><span data-stu-id="9cec1-713">The oplock request is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-714"><span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**ERRO \_ de \_ protocolo oplock inválido \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-714"><span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**ERROR\_INVALID\_OPLOCK\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-715">301 (0x12D)</span><span class="sxs-lookup"><span data-stu-id="9cec1-715">301 (0x12D)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-716">Uma confirmação de oplock inválida foi recebida pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="9cec1-716">An invalid oplock acknowledgment was received by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-717"><span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**disco de erro \_ \_ muito \_ fragmentado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-717"><span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**ERROR\_DISK\_TOO\_FRAGMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-718">302 (0x12E)</span><span class="sxs-lookup"><span data-stu-id="9cec1-718">302 (0x12E)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-719">O volume está muito fragmentado para concluir esta operação.</span><span class="sxs-lookup"><span data-stu-id="9cec1-719">The volume is too fragmented to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-720"><span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**ERRO ao \_ excluir \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="9cec1-720"><span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**ERROR\_DELETE\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-721">303 (0x12F)</span><span class="sxs-lookup"><span data-stu-id="9cec1-721">303 (0x12F)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-722">O arquivo não pode ser aberto porque está em processo de exclusão.</span><span class="sxs-lookup"><span data-stu-id="9cec1-722">The file cannot be opened because it is in the process of being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-723"><span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**ERRO \_ incompatível \_ com \_ a \_ \_ configuração de \_ registro de nome curto global \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-723"><span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**ERROR\_INCOMPATIBLE\_WITH\_GLOBAL\_SHORT\_NAME\_REGISTRY\_SETTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-724">304 (0x130)</span><span class="sxs-lookup"><span data-stu-id="9cec1-724">304 (0x130)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-725">As configurações de nome curto não podem ser alteradas neste volume devido à configuração do registro global.</span><span class="sxs-lookup"><span data-stu-id="9cec1-725">Short name settings may not be changed on this volume due to the global registry setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-726"><span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**\_nomes curtos \_ \_ de erro não \_ habilitados \_ no \_ volume**</span><span class="sxs-lookup"><span data-stu-id="9cec1-726"><span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**ERROR\_SHORT\_NAMES\_NOT\_ENABLED\_ON\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-727">305 (0x131)</span><span class="sxs-lookup"><span data-stu-id="9cec1-727">305 (0x131)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-728">Os nomes curtos não estão habilitados neste volume.</span><span class="sxs-lookup"><span data-stu-id="9cec1-728">Short names are not enabled on this volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-729"><span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**o \_ fluxo de segurança do erro \_ \_ está \_ inconsistente**</span><span class="sxs-lookup"><span data-stu-id="9cec1-729"><span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**ERROR\_SECURITY\_STREAM\_IS\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-730">306 (0x132)</span><span class="sxs-lookup"><span data-stu-id="9cec1-730">306 (0x132)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-731">O fluxo de segurança para o volume especificado está em um estado inconsistente.</span><span class="sxs-lookup"><span data-stu-id="9cec1-731">The security stream for the given volume is in an inconsistent state.</span></span> <span data-ttu-id="9cec1-732">Execute CHKDSK no volume.</span><span class="sxs-lookup"><span data-stu-id="9cec1-732">Please run CHKDSK on the volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-733"><span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**ERRO \_ de \_ intervalo de bloqueio inválido \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-733"><span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**ERROR\_INVALID\_LOCK\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-734">307 (0x133)</span><span class="sxs-lookup"><span data-stu-id="9cec1-734">307 (0x133)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-735">Uma operação de bloqueio de arquivo solicitada não pode ser processada devido a um intervalo de bytes inválido.</span><span class="sxs-lookup"><span data-stu-id="9cec1-735">A requested file lock operation cannot be processed due to an invalid byte range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-736"><span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**o \_ SUBsistema de imagem de erro \_ \_ não \_ está presente**</span><span class="sxs-lookup"><span data-stu-id="9cec1-736"><span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**ERROR\_IMAGE\_SUBSYSTEM\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-737">308 (0x134)</span><span class="sxs-lookup"><span data-stu-id="9cec1-737">308 (0x134)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-738">O subsistema necessário para dar suporte ao tipo de imagem não está presente.</span><span class="sxs-lookup"><span data-stu-id="9cec1-738">The subsystem needed to support the image type is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-739"><span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**GUID de notificação de erro \_ \_ \_ já \_ definido**</span><span class="sxs-lookup"><span data-stu-id="9cec1-739"><span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**ERROR\_NOTIFICATION\_GUID\_ALREADY\_DEFINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-740">309 (0x135)</span><span class="sxs-lookup"><span data-stu-id="9cec1-740">309 (0x135)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-741">O arquivo especificado já tem um GUID de notificação associado a ele.</span><span class="sxs-lookup"><span data-stu-id="9cec1-741">The specified file already has a notification GUID associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-742"><span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**ERRO \_ de \_ manipulador de exceção inválido \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-742"><span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**ERROR\_INVALID\_EXCEPTION\_HANDLER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-743">310 (0x136)</span><span class="sxs-lookup"><span data-stu-id="9cec1-743">310 (0x136)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-744">Uma rotina de manipulador de exceção inválida foi detectada.</span><span class="sxs-lookup"><span data-stu-id="9cec1-744">An invalid exception handler routine has been detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-745"><span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**ERRO de \_ duplicação de \_ privilégios**</span><span class="sxs-lookup"><span data-stu-id="9cec1-745"><span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**ERROR\_DUPLICATE\_PRIVILEGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-746">311 (0x137)</span><span class="sxs-lookup"><span data-stu-id="9cec1-746">311 (0x137)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-747">Foram especificados privilégios duplicados para o token.</span><span class="sxs-lookup"><span data-stu-id="9cec1-747">Duplicate privileges were specified for the token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-748"><span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**ERRO \_ nenhum \_ intervalo \_ processado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-748"><span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**ERROR\_NO\_RANGES\_PROCESSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-749">312 (0x138)</span><span class="sxs-lookup"><span data-stu-id="9cec1-749">312 (0x138)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-750">Nenhum intervalo para a operação especificada pôde ser processado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-750">No ranges for the specified operation were able to be processed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-751"><span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**ERRO \_ não \_ permitido \_ no \_ arquivo do sistema \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-751"><span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**ERROR\_NOT\_ALLOWED\_ON\_SYSTEM\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-752">313 (0x139)</span><span class="sxs-lookup"><span data-stu-id="9cec1-752">313 (0x139)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-753">A operação não é permitida em um arquivo interno do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="9cec1-753">Operation is not allowed on a file system internal file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-754"><span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**recursos de disco de erro \_ \_ \_ esgotados**</span><span class="sxs-lookup"><span data-stu-id="9cec1-754"><span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**ERROR\_DISK\_RESOURCES\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-755">314 (0x13A)</span><span class="sxs-lookup"><span data-stu-id="9cec1-755">314 (0x13A)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-756">Os recursos físicos deste disco foram esgotados.</span><span class="sxs-lookup"><span data-stu-id="9cec1-756">The physical resources of this disk have been exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-757"><span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**\_token inválido do erro \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-757"><span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**ERROR\_INVALID\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-758">315 (0x13B)</span><span class="sxs-lookup"><span data-stu-id="9cec1-758">315 (0x13B)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-759">O token que representa os dados é inválido.</span><span class="sxs-lookup"><span data-stu-id="9cec1-759">The token representing the data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-760"><span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**recurso de dispositivo de erro \_ \_ \_ sem \_ suporte**</span><span class="sxs-lookup"><span data-stu-id="9cec1-760"><span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**ERROR\_DEVICE\_FEATURE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-761">316 (0x13C)</span><span class="sxs-lookup"><span data-stu-id="9cec1-761">316 (0x13C)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-762">O dispositivo não oferece suporte ao recurso de comando.</span><span class="sxs-lookup"><span data-stu-id="9cec1-762">The device does not support the command feature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-763"><span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**ERRO \_ Mr \_ mid \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-763"><span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**ERROR\_MR\_MID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-764">317 (0x13D)</span><span class="sxs-lookup"><span data-stu-id="9cec1-764">317 (0x13D)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-765">O sistema não pode encontrar o texto da mensagem para o número de mensagem 0x %1 no arquivo de mensagem para %2.</span><span class="sxs-lookup"><span data-stu-id="9cec1-765">The system cannot find message text for message number 0x%1 in the message file for %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-766"><span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**escopo de erro \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="9cec1-766"><span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**ERROR\_SCOPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-767">318 (0x13E)</span><span class="sxs-lookup"><span data-stu-id="9cec1-767">318 (0x13E)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-768">O escopo especificado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-768">The scope specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-769"><span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**ERRO de \_ escopo INdefinido \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-769"><span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**ERROR\_UNDEFINED\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-770">319 (0x13F)</span><span class="sxs-lookup"><span data-stu-id="9cec1-770">319 (0x13F)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-771">A política de acesso central especificada não está definida no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="9cec1-771">The Central Access Policy specified is not defined on the target machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-772"><span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**\_limite inválido de erro \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-772"><span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**ERROR\_INVALID\_CAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-773">320 (0x140)</span><span class="sxs-lookup"><span data-stu-id="9cec1-773">320 (0x140)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-774">A política de acesso central Obtida de Active Directory é inválida.</span><span class="sxs-lookup"><span data-stu-id="9cec1-774">The Central Access Policy obtained from Active Directory is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-775"><span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**dispositivo de erro \_ \_ inacessível**</span><span class="sxs-lookup"><span data-stu-id="9cec1-775"><span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**ERROR\_DEVICE\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-776">321 (0x141)</span><span class="sxs-lookup"><span data-stu-id="9cec1-776">321 (0x141)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-777">O dispositivo está inacessível.</span><span class="sxs-lookup"><span data-stu-id="9cec1-777">The device is unreachable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-778"><span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**dispositivo de erro \_ \_ sem \_ recursos**</span><span class="sxs-lookup"><span data-stu-id="9cec1-778"><span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**ERROR\_DEVICE\_NO\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-779">322 (0x142)</span><span class="sxs-lookup"><span data-stu-id="9cec1-779">322 (0x142)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-780">O dispositivo de destino tem recursos insuficientes para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="9cec1-780">The target device has insufficient resources to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-781"><span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**\_erro de \_ checksum de dados de erro \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-781"><span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**ERROR\_DATA\_CHECKSUM\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-782">323 (0x143)</span><span class="sxs-lookup"><span data-stu-id="9cec1-782">323 (0x143)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-783">Ocorreu um erro de soma de verificação de integridade de dados.</span><span class="sxs-lookup"><span data-stu-id="9cec1-783">A data integrity checksum error occurred.</span></span> <span data-ttu-id="9cec1-784">Os dados no fluxo de arquivos estão corrompidos.</span><span class="sxs-lookup"><span data-stu-id="9cec1-784">Data in the file stream is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-785"><span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**ERRO de \_ operação de ea de kernel INTERmisturada \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-785"><span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**ERROR\_INTERMIXED\_KERNEL\_EA\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-786">324 (0x144)</span><span class="sxs-lookup"><span data-stu-id="9cec1-786">324 (0x144)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-787">Foi feita uma tentativa de modificar um KERNEL e um EA (atributo estendido normal) na mesma operação.</span><span class="sxs-lookup"><span data-stu-id="9cec1-787">An attempt was made to modify both a KERNEL and normal Extended Attribute (EA) in the same operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-788"><span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**corte de nível de arquivo de erro \_ \_ \_ \_ sem \_ suporte**</span><span class="sxs-lookup"><span data-stu-id="9cec1-788"><span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**ERROR\_FILE\_LEVEL\_TRIM\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-789">326 (0x146)</span><span class="sxs-lookup"><span data-stu-id="9cec1-789">326 (0x146)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-790">O dispositivo não dá suporte ao corte em nível de arquivo.</span><span class="sxs-lookup"><span data-stu-id="9cec1-790">Device does not support file-level TRIM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-791"><span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**\_violação de \_ alinhamento de deslocamento de erro \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-791"><span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**ERROR\_OFFSET\_ALIGNMENT\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-792">327 (0x147)</span><span class="sxs-lookup"><span data-stu-id="9cec1-792">327 (0x147)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-793">O comando especificou um deslocamento de dados que não se alinha à granularidade/alinhamento do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9cec1-793">The command specified a data offset that does not align to the device's granularity/alignment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-794"><span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**ERRO \_ \_ de campo \_ inválido \_ na \_ lista de parâmetros**</span><span class="sxs-lookup"><span data-stu-id="9cec1-794"><span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**ERROR\_INVALID\_FIELD\_IN\_PARAMETER\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-795">328 (0x148)</span><span class="sxs-lookup"><span data-stu-id="9cec1-795">328 (0x148)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-796">O comando especificou um campo inválido em sua lista de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9cec1-796">The command specified an invalid field in its parameter list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-797"><span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**\_operação \_ de erro em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="9cec1-797"><span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**ERROR\_OPERATION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-798">329 (0x149)</span><span class="sxs-lookup"><span data-stu-id="9cec1-798">329 (0x149)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-799">Uma operação está em andamento no momento com o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9cec1-799">An operation is currently in progress with the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-800"><span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**ERRO \_ de \_ caminho de dispositivo insatisfatório \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-800"><span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**ERROR\_BAD\_DEVICE\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-801">330 (0x14A)</span><span class="sxs-lookup"><span data-stu-id="9cec1-801">330 (0x14A)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-802">Foi feita uma tentativa de enviar o comando por meio de um caminho inválido para o dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="9cec1-802">An attempt was made to send down the command via an invalid path to the target device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-803"><span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**ERRO \_ em \_ muitos \_ descritores**</span><span class="sxs-lookup"><span data-stu-id="9cec1-803"><span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**ERROR\_TOO\_MANY\_DESCRIPTORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-804">331 (0x14B)</span><span class="sxs-lookup"><span data-stu-id="9cec1-804">331 (0x14B)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-805">O comando especificou um número de descritores que excederam o máximo com suporte do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9cec1-805">The command specified a number of descriptors that exceeded the maximum supported by the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-806"><span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**dados de limpeza de erro \_ \_ \_ desabilitados**</span><span class="sxs-lookup"><span data-stu-id="9cec1-806"><span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**ERROR\_SCRUB\_DATA\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-807">332 (0x14C)</span><span class="sxs-lookup"><span data-stu-id="9cec1-807">332 (0x14C)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-808">A limpeza está desabilitada no arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-808">Scrub is disabled on the specified file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-809"><span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**ERRO \_ não \_ \_ armazenamento redundante**</span><span class="sxs-lookup"><span data-stu-id="9cec1-809"><span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**ERROR\_NOT\_REDUNDANT\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-810">333 (0x14D)</span><span class="sxs-lookup"><span data-stu-id="9cec1-810">333 (0x14D)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-811">O dispositivo de armazenamento não fornece redundância.</span><span class="sxs-lookup"><span data-stu-id="9cec1-811">The storage device does not provide redundancy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-812"><span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**\_arquivo residente de erro \_ \_ sem \_ suporte**</span><span class="sxs-lookup"><span data-stu-id="9cec1-812"><span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**ERROR\_RESIDENT\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-813">334 (0x14E)</span><span class="sxs-lookup"><span data-stu-id="9cec1-813">334 (0x14E)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-814">Não há suporte para uma operação em um arquivo residente.</span><span class="sxs-lookup"><span data-stu-id="9cec1-814">An operation is not supported on a resident file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-815"><span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**ERRO \_ arquivo compactado \_ \_ sem \_ suporte**</span><span class="sxs-lookup"><span data-stu-id="9cec1-815"><span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**ERROR\_COMPRESSED\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-816">335 (0x14F)</span><span class="sxs-lookup"><span data-stu-id="9cec1-816">335 (0x14F)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-817">Não há suporte para uma operação em um arquivo compactado.</span><span class="sxs-lookup"><span data-stu-id="9cec1-817">An operation is not supported on a compressed file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-818"><span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**\_ \_ não \_ há suporte para o diretório de erros**</span><span class="sxs-lookup"><span data-stu-id="9cec1-818"><span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**ERROR\_DIRECTORY\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-819">336 (0x150)</span><span class="sxs-lookup"><span data-stu-id="9cec1-819">336 (0x150)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-820">Não há suporte para uma operação em um diretório.</span><span class="sxs-lookup"><span data-stu-id="9cec1-820">An operation is not supported on a directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-821"><span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**ERRO \_ não \_ lido \_ da \_ cópia**</span><span class="sxs-lookup"><span data-stu-id="9cec1-821"><span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**ERROR\_NOT\_READ\_FROM\_COPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-822">337 (0x151)</span><span class="sxs-lookup"><span data-stu-id="9cec1-822">337 (0x151)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-823">Não foi possível ler a cópia especificada dos dados solicitados.</span><span class="sxs-lookup"><span data-stu-id="9cec1-823">The specified copy of the requested data could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-824"><span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**ERRO \_ falha na \_ \_ reinicialização de ação**</span><span class="sxs-lookup"><span data-stu-id="9cec1-824"><span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**ERROR\_FAIL\_NOACTION\_REBOOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-825">350 (0x15E)</span><span class="sxs-lookup"><span data-stu-id="9cec1-825">350 (0x15E)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-826">Nenhuma ação foi executada porque uma reinicialização do sistema é necessária.</span><span class="sxs-lookup"><span data-stu-id="9cec1-826">No action was taken as a system reboot is required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-827"><span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**\_falha no \_ desligamento do erro**</span><span class="sxs-lookup"><span data-stu-id="9cec1-827"><span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**ERROR\_FAIL\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-828">351 (0x15F)</span><span class="sxs-lookup"><span data-stu-id="9cec1-828">351 (0x15F)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-829">Falha na operação de desligamento.</span><span class="sxs-lookup"><span data-stu-id="9cec1-829">The shutdown operation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-830"><span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**ERRO \_ falha ao \_ reiniciar**</span><span class="sxs-lookup"><span data-stu-id="9cec1-830"><span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**ERROR\_FAIL\_RESTART**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-831">352 (0x160)</span><span class="sxs-lookup"><span data-stu-id="9cec1-831">352 (0x160)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-832">Falha na operação de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="9cec1-832">The restart operation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-833"><span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**ERRO \_ máximo de \_ sessões \_ atingido**</span><span class="sxs-lookup"><span data-stu-id="9cec1-833"><span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**ERROR\_MAX\_SESSIONS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-834">353 (0x161)</span><span class="sxs-lookup"><span data-stu-id="9cec1-834">353 (0x161)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-835">O número máximo de sessões foi atingido.</span><span class="sxs-lookup"><span data-stu-id="9cec1-835">The maximum number of sessions has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-836"><span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**modo de thread de erro \_ \_ \_ já \_ em segundo plano**</span><span class="sxs-lookup"><span data-stu-id="9cec1-836"><span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**ERROR\_THREAD\_MODE\_ALREADY\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-837">400 (0x190)</span><span class="sxs-lookup"><span data-stu-id="9cec1-837">400 (0x190)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-838">O thread já está no modo de processamento em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="9cec1-838">The thread is already in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-839"><span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**modo de thread de erro \_ \_ \_ não \_ em segundo plano**</span><span class="sxs-lookup"><span data-stu-id="9cec1-839"><span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**ERROR\_THREAD\_MODE\_NOT\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-840">401 (0x191)</span><span class="sxs-lookup"><span data-stu-id="9cec1-840">401 (0x191)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-841">O thread não está no modo de processamento em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="9cec1-841">The thread is not in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-842"><span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**modo de processo de erro \_ \_ \_ já \_ em segundo plano**</span><span class="sxs-lookup"><span data-stu-id="9cec1-842"><span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**ERROR\_PROCESS\_MODE\_ALREADY\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-843">402 (0x192)</span><span class="sxs-lookup"><span data-stu-id="9cec1-843">402 (0x192)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-844">O processo já está no modo de processamento em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="9cec1-844">The process is already in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-845"><span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**modo de processo de erro \_ \_ \_ não \_ em segundo plano**</span><span class="sxs-lookup"><span data-stu-id="9cec1-845"><span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**ERROR\_PROCESS\_MODE\_NOT\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-846">403 (0x193)</span><span class="sxs-lookup"><span data-stu-id="9cec1-846">403 (0x193)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-847">O processo não está no modo de processamento em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="9cec1-847">The process is not in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9cec1-848"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**\_endereço inválido do erro \_**</span><span class="sxs-lookup"><span data-stu-id="9cec1-848"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR\_INVALID\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cec1-849">487 (0x1E7)</span><span class="sxs-lookup"><span data-stu-id="9cec1-849">487 (0x1E7)</span></span>
</dt> <dt>



<span data-ttu-id="9cec1-850">Tentativa de acessar endereço inválido.</span><span class="sxs-lookup"><span data-stu-id="9cec1-850">Attempt to access invalid address.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="9cec1-851">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cec1-851">Requirements</span></span>



| <span data-ttu-id="9cec1-852">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cec1-852">Requirement</span></span> | <span data-ttu-id="9cec1-853">Valor</span><span class="sxs-lookup"><span data-stu-id="9cec1-853">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cec1-854">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cec1-854">Minimum supported client</span></span><br/> | <span data-ttu-id="9cec1-855">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9cec1-855">Windows XP \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="9cec1-856">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cec1-856">Minimum supported server</span></span><br/> | <span data-ttu-id="9cec1-857">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9cec1-857">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9cec1-858">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9cec1-858">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cec1-859"><dt>WinError. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9cec1-859"><dt>WinError.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cec1-860">Confira também</span><span class="sxs-lookup"><span data-stu-id="9cec1-860">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cec1-861">Códigos de erro do sistema</span><span class="sxs-lookup"><span data-stu-id="9cec1-861">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




