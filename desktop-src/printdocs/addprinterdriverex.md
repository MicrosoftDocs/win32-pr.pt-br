---
description: A função AddPrinterDriverEx instala um driver de impressora local ou remota e vincula a configuração, os dados e os arquivos de driver.
ms.assetid: 472adb7d-39cc-4c76-b96c-610ff9d276ad
title: Função AddPrinterDriverEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriverEx
- AddPrinterDriverExA
- AddPrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c431d710ddad7f723d063fd5bf046bae08b77b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757654"
---
# <a name="addprinterdriverex-function"></a><span data-ttu-id="1a507-103">Função AddPrinterDriverEx</span><span class="sxs-lookup"><span data-stu-id="1a507-103">AddPrinterDriverEx function</span></span>

<span data-ttu-id="1a507-104">A função **AddPrinterDriverEx** instala um driver de impressora local ou remota e vincula a configuração, os dados e os arquivos de driver.</span><span class="sxs-lookup"><span data-stu-id="1a507-104">The **AddPrinterDriverEx** function installs a local or remote printer driver and links the configuration, data, and driver files.</span></span> <span data-ttu-id="1a507-105">Além de ter os recursos do [**AddPrinterDriver**](addprinterdriver.md), ele também tem opções que permitem a atualização estrita, o downgrade estrito, a cópia de arquivos mais recentes e a cópia de todos os arquivos (independentemente dos carimbos de data/hora do arquivo).</span><span class="sxs-lookup"><span data-stu-id="1a507-105">Besides having the capabilities of [**AddPrinterDriver**](addprinterdriver.md), it also has options that permit strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of file time stamps).</span></span>

> [!Note]  
> <span data-ttu-id="1a507-106">A instalação de um driver de impressora sem um pacote de driver não é mais recomendada.</span><span class="sxs-lookup"><span data-stu-id="1a507-106">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="1a507-107">Use [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="1a507-107">Use [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) instead.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1a507-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a507-108">Syntax</span></span>


```C++
BOOL AddPrinterDriverEx(
  _In_    LPTSTR pName,
  _In_    DWORD  Level,
  _Inout_ LPBYTE pDriverInfo,
  _In_    DWORD  dwFileCopyFlags
);
```



## <a name="parameters"></a><span data-ttu-id="1a507-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a507-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a507-110">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1a507-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a507-111">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual o driver deve ser instalado.</span><span class="sxs-lookup"><span data-stu-id="1a507-111">A pointer to a null-terminated string that specifies the name of the server on which the driver should be installed.</span></span> <span data-ttu-id="1a507-112">Se esse parâmetro for **nulo**, a função instalará o driver no computador local.</span><span class="sxs-lookup"><span data-stu-id="1a507-112">If this parameter is **NULL**, the function installs the driver on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="1a507-113">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="1a507-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a507-114">A versão da estrutura à qual o *pDriverInfo* aponta.</span><span class="sxs-lookup"><span data-stu-id="1a507-114">The version of the structure to which *pDriverInfo* points.</span></span> <span data-ttu-id="1a507-115">Esse valor pode ser 2, 3, 4, 6 ou 8.</span><span class="sxs-lookup"><span data-stu-id="1a507-115">This value can be 2, 3, 4, 6, or 8.</span></span>

</dd> <dt>

<span data-ttu-id="1a507-116">*pDriverInfo* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="1a507-116">*pDriverInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a507-117">Um ponteiro para uma estrutura que contém informações de driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="1a507-117">A pointer to a structure containing printer driver information.</span></span> <span data-ttu-id="1a507-118">Pode ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="1a507-118">It can be one of the following.</span></span>



| <span data-ttu-id="1a507-119">Valor do nível</span><span class="sxs-lookup"><span data-stu-id="1a507-119">Value of Level</span></span>                                                                                       | <span data-ttu-id="1a507-120">\_Estrutura de informações do driver \_ \*</span><span class="sxs-lookup"><span data-stu-id="1a507-120">DRIVER\_INFO\_\* Structure</span></span>                          |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="2"></span><dl> <span data-ttu-id="1a507-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="1a507-121"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="1a507-122">**Informações do DRIVER \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="1a507-122">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="1a507-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="1a507-123"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="1a507-124">**Informações do DRIVER \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="1a507-124">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="1a507-125"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="1a507-125"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="1a507-126">**Informações do DRIVER \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="1a507-126">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="1a507-127"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="1a507-127"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="1a507-128">**Informações do DRIVER \_ \_ 6**</span><span class="sxs-lookup"><span data-stu-id="1a507-128">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="1a507-129"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="1a507-129"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="1a507-130">**Informações do DRIVER \_ \_ 8**</span><span class="sxs-lookup"><span data-stu-id="1a507-130">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

<span data-ttu-id="1a507-131">Se o membro **pEnvironment** da estrutura apontada por *pDriverInfo* for **NULL**, a função usará o ambiente atual do chamador/cliente, não o ambiente do destino/servidor.</span><span class="sxs-lookup"><span data-stu-id="1a507-131">If the **pEnvironment** member of the structure pointed to by *pDriverInfo* is **NULL**, the function uses the current environment of the caller/client, not the environment of the destination/server.</span></span>

</dd> <dt>

<span data-ttu-id="1a507-132">*dwFileCopyFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1a507-132">*dwFileCopyFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a507-133">As opções para copiar os arquivos de driver.</span><span class="sxs-lookup"><span data-stu-id="1a507-133">The options for copying the driver files.</span></span> <span data-ttu-id="1a507-134">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1a507-134">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="1a507-135">Valor</span><span class="sxs-lookup"><span data-stu-id="1a507-135">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="1a507-136">Significado</span><span class="sxs-lookup"><span data-stu-id="1a507-136">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APD_COPY_ALL_FILES"></span><span id="apd_copy_all_files"></span><dl> <span data-ttu-id="1a507-137"><dt>**APD \_ copiar \_ todos os \_ arquivos**</dt></span><span class="sxs-lookup"><span data-stu-id="1a507-137"><dt>**APD\_COPY\_ALL\_FILES**</dt></span></span> </dl>                | <span data-ttu-id="1a507-138">Adicione o driver de impressora e copie todos os arquivos no diretório de driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="1a507-138">Add the printer driver and copy all the files in the printer-driver directory.</span></span> <span data-ttu-id="1a507-139">Os carimbos de data/hora do arquivo são ignorados com essa opção.</span><span class="sxs-lookup"><span data-stu-id="1a507-139">The file time stamps are ignored with this option.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="APD_COPY_FROM_DIRECTORY"></span><span id="apd_copy_from_directory"></span><dl> <span data-ttu-id="1a507-140"><dt>**APD \_ copiar \_ do \_ diretório**</dt></span><span class="sxs-lookup"><span data-stu-id="1a507-140"><dt>**APD\_COPY\_FROM\_DIRECTORY**</dt></span></span> </dl> | <span data-ttu-id="1a507-141">Adicione o driver de impressora usando os nomes de arquivo totalmente qualificados especificados na estrutura [**informações do driver \_ \_ 6**](driver-info-6.md) .</span><span class="sxs-lookup"><span data-stu-id="1a507-141">Add the printer driver using the fully qualified file names specified in the [**DRIVER\_INFO\_6**](driver-info-6.md) structure.</span></span> <span data-ttu-id="1a507-142">Esse sinalizador é vinculada em conjunto com um dos outros sinalizadores de cópia.</span><span class="sxs-lookup"><span data-stu-id="1a507-142">This flag is ORed in conjunction with one of the other copy flags.</span></span> <span data-ttu-id="1a507-143">Se esse sinalizador for definido, **AddPrinterDriverEx** falhará se os arquivos não existirem onde eles estiverem especificados na estrutura informações do **Driver \_ \_ 6** .</span><span class="sxs-lookup"><span data-stu-id="1a507-143">If this flag is set, **AddPrinterDriverEx** will fail if the files do not exist where they are specified to exist by the **DRIVER\_INFO\_6** structure.</span></span> <span data-ttu-id="1a507-144">Os arquivos não precisam ser copiados para o diretório do driver de impressora do sistema.</span><span class="sxs-lookup"><span data-stu-id="1a507-144">The files do not need to be copied to the system's printer-driver directory.</span></span> <span data-ttu-id="1a507-145">Consulte os comentários.</span><span class="sxs-lookup"><span data-stu-id="1a507-145">See the Remarks.</span></span><br/> <span data-ttu-id="1a507-146">**Windows 2000:** Não há suporte para esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="1a507-146">**Windows 2000:** This flag is not supported.</span></span><br/> |
| <span id="APD_COPY_NEW_FILES"></span><span id="apd_copy_new_files"></span><dl> <span data-ttu-id="1a507-147"><dt>**APD \_ copiar \_ novos \_ arquivos**</dt></span><span class="sxs-lookup"><span data-stu-id="1a507-147"><dt>**APD\_COPY\_NEW\_FILES**</dt></span></span> </dl>                | <span data-ttu-id="1a507-148">Adicione o driver de impressora e copie os arquivos no diretório de driver de impressora que são mais novos do que os arquivos correspondentes que estão em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="1a507-148">Add the printer driver and copy the files in the printer-driver directory that are newer than any corresponding files that are currently in use.</span></span> <span data-ttu-id="1a507-149">Esse sinalizador emula o comportamento de [**AddPrinterDriver**](addprinterdriver.md).</span><span class="sxs-lookup"><span data-stu-id="1a507-149">This flag emulates the behavior of [**AddPrinterDriver**](addprinterdriver.md).</span></span><br/>                                                                                                                                                                                                                                                                                  |
| <span id="APD_STRICT_DOWNGRADE"></span><span id="apd_strict_downgrade"></span><dl> <span data-ttu-id="1a507-150"><dt>**\_downgrade estrito \_ APD**</dt></span><span class="sxs-lookup"><span data-stu-id="1a507-150"><dt>**APD\_STRICT\_DOWNGRADE**</dt></span></span> </dl>           | <span data-ttu-id="1a507-151">Adicione o driver de impressora somente se todos os arquivos no diretório de driver de impressora forem mais antigos do que quaisquer arquivos correspondentes em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="1a507-151">Add the printer driver only if all the files in the printer-driver directory are older than any corresponding files currently in use.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="APD_STRICT_UPGRADE"></span><span id="apd_strict_upgrade"></span><dl> <span data-ttu-id="1a507-152"><dt>**APD \_ de \_ atualização estrita**</dt></span><span class="sxs-lookup"><span data-stu-id="1a507-152"><dt>**APD\_STRICT\_UPGRADE**</dt></span></span> </dl>                 | <span data-ttu-id="1a507-153">Adicione o driver de impressora somente se todos os arquivos no diretório de driver de impressora forem mais novos do que os arquivos correspondentes em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="1a507-153">Add the printer driver only if all the files in the printer-driver directory are newer than any corresponding files currently in use.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a507-154">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1a507-154">Return value</span></span>

<span data-ttu-id="1a507-155">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="1a507-155">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="1a507-156">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="1a507-156">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="1a507-157">Se o driver de impressora tiver problemas para funcionar com o sistema operacional, o **AddPrinterDriverEx** falhará com um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="1a507-157">If the printer driver is known to have problems working with the operating system, **AddPrinterDriverEx** will fail with one of the following error codes:</span></span>



| <span data-ttu-id="1a507-158">Código do Erro</span><span class="sxs-lookup"><span data-stu-id="1a507-158">Error Code</span></span>                      | <span data-ttu-id="1a507-159">Significado</span><span class="sxs-lookup"><span data-stu-id="1a507-159">Meaning</span></span>                                                                                                                                                   |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a507-160">Driver de impressora de erro \_ \_ \_ bloqueado</span><span class="sxs-lookup"><span data-stu-id="1a507-160">ERROR\_PRINTER\_DRIVER\_BLOCKED</span></span> | <span data-ttu-id="1a507-161">O driver não funciona no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1a507-161">The driver does not work on the operating system.</span></span>                                                                                                         |
| <span data-ttu-id="1a507-162">ERRO \_ de \_ Driver de impressora \_ avisado</span><span class="sxs-lookup"><span data-stu-id="1a507-162">ERROR\_PRINTER\_DRIVER\_WARNED</span></span>  | <span data-ttu-id="1a507-163">O driver não é confiável no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1a507-163">The driver is unreliable on the operating system.</span></span> <span data-ttu-id="1a507-164">No entanto, se APD \_ instalar \_ \_ o driver avisado for especificado, o driver será instalado e nenhum aviso será fornecido.</span><span class="sxs-lookup"><span data-stu-id="1a507-164">However, if APD\_INSTALL\_WARNED\_DRIVER is specified, the driver is installed and no warning is given.</span></span> |



 

<span data-ttu-id="1a507-165">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="1a507-165">For more information, see the Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a507-166">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a507-166">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1a507-167">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="1a507-167">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="1a507-168">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1a507-168">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="1a507-169">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="1a507-169">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="1a507-170">O chamador deve ter o [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="1a507-170">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="1a507-171">Antes de chamar a função **AddPrinterDriverEx** , todos os arquivos exigidos pelo driver devem ser copiados para o diretório de driver de impressora do sistema.</span><span class="sxs-lookup"><span data-stu-id="1a507-171">Before calling the **AddPrinterDriverEx** function, all files required by the driver must be copied to the system's printer-driver directory.</span></span> <span data-ttu-id="1a507-172">Para recuperar o nome desse diretório, chame a função [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="1a507-172">To retrieve the name of this directory, call the [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) function.</span></span>

<span data-ttu-id="1a507-173">Para determinar quais drivers de impressora estão instalados no momento, chame a função [**EnumPrinterDrivers**](enumprinterdrivers.md) .</span><span class="sxs-lookup"><span data-stu-id="1a507-173">To determine which printer drivers are currently installed, call the [**EnumPrinterDrivers**](enumprinterdrivers.md) function.</span></span>

<span data-ttu-id="1a507-174">Se o driver de impressora tiver sido adicionado com êxito, a função chamará a função DrvDriverEvent (inicialização de evento de DRIVER \_ \_ , nível, \_ informações \_ \* de driver, lParam) para permitir que o driver execute as inicializações necessárias durante a instalação de um driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="1a507-174">If the printer driver has been successfully added, the function calls the DrvDriverEvent (DRIVER\_EVENT\_INITIALIZE, Level, DRIVER\_INFO\_\*, lparam ) function to allow the driver to perform any initializations required during the installation of a printer driver.</span></span> <span data-ttu-id="1a507-175">Para obter mais informações sobre o **DrvDriverEvent**, consulte o Microsoft Windows Driver Development Kit (DDK)</span><span class="sxs-lookup"><span data-stu-id="1a507-175">For more information about **DrvDriverEvent**, see the Microsoft Windows Driver Development Kit (DDK)</span></span>

<span data-ttu-id="1a507-176">O driver não deve usar uma chamada de interface do usuário durante a chamada para **DrvDriverEvent**.</span><span class="sxs-lookup"><span data-stu-id="1a507-176">The driver should not use a UI call during the call to **DrvDriverEvent**.</span></span> <span data-ttu-id="1a507-177">Para fazer trabalhos relacionados à interface do usuário, o instalador deve usar a entrada VendorSetup no arquivo. inf da impressora ou, para dispositivos Plug and Play, o instalador pode usar um coinstalador específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1a507-177">To do UI-related jobs, the installer should either use the VendorSetup entry in the printer's .inf file or, for Plug and Play devices, the installer can use a device-specific co-installer.</span></span> <span data-ttu-id="1a507-178">Para obter mais informações sobre VendorSetup, consulte o DDK.</span><span class="sxs-lookup"><span data-stu-id="1a507-178">For more information about VendorSetup, see the DDK.</span></span>

<span data-ttu-id="1a507-179">Os arquivos que são referenciados na [**estrutura \_ informações \_ sobre o driver 6**](driver-info-6.md) devem ser locais no computador do qual a chamada é feita.</span><span class="sxs-lookup"><span data-stu-id="1a507-179">The files that are referenced in the [**DRIVER\_INFO\_6**](driver-info-6.md) structure must be local to the machine from which the call is made.</span></span> <span data-ttu-id="1a507-180">Um nome de arquivo pode ser um nome UNC, desde que o nome UNC seja o computador local.</span><span class="sxs-lookup"><span data-stu-id="1a507-180">A file name can be a UNC name as long as the UNC name is the local machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a507-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a507-181">Requirements</span></span>



| <span data-ttu-id="1a507-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a507-182">Requirement</span></span> | <span data-ttu-id="1a507-183">Valor</span><span class="sxs-lookup"><span data-stu-id="1a507-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a507-184">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a507-184">Minimum supported client</span></span><br/> | <span data-ttu-id="1a507-185">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1a507-185">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1a507-186">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a507-186">Minimum supported server</span></span><br/> | <span data-ttu-id="1a507-187">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1a507-187">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1a507-188">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1a507-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a507-189"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a507-189"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1a507-190">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1a507-190">Library</span></span><br/>                  | <dl> <span data-ttu-id="1a507-191"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a507-191"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="1a507-192">DLL</span><span class="sxs-lookup"><span data-stu-id="1a507-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a507-193"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="1a507-193"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="1a507-194">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="1a507-194">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1a507-195">**AddPrinterDriverExW** (Unicode) e **AddPrinterDriverExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1a507-195">**AddPrinterDriverExW** (Unicode) and **AddPrinterDriverExA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="1a507-196">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a507-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a507-197">Impressão</span><span class="sxs-lookup"><span data-stu-id="1a507-197">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1a507-198">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="1a507-198">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="1a507-199">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="1a507-199">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="1a507-200">**Informações do DRIVER \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="1a507-200">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="1a507-201">**Informações do DRIVER \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="1a507-201">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="1a507-202">**Informações do DRIVER \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="1a507-202">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="1a507-203">**Informações do DRIVER \_ \_ 6**</span><span class="sxs-lookup"><span data-stu-id="1a507-203">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="1a507-204">**DeletePrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="1a507-204">**DeletePrinterDriverEx**</span></span>](deleteprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="1a507-205">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="1a507-205">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="1a507-206">**GetPrinterDriverDirectory**</span><span class="sxs-lookup"><span data-stu-id="1a507-206">**GetPrinterDriverDirectory**</span></span>](getprinterdriverdirectory.md)
</dt> </dl>

 

