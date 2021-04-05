---
description: A função AddPrinterDriver instala um driver de impressora local ou remoto e associa a configuração, os dados e os arquivos de driver.
ms.assetid: 0f762800-f5a5-40ea-8be1-7fd8bda23788
title: Função AddPrinterDriver (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriver
- AddPrinterDriverA
- AddPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: de5a9e9d16a47dfe8b9620edc9acdc5c5fd4d552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662608"
---
# <a name="addprinterdriver-function"></a><span data-ttu-id="69d65-103">Função AddPrinterDriver</span><span class="sxs-lookup"><span data-stu-id="69d65-103">AddPrinterDriver function</span></span>

<span data-ttu-id="69d65-104">A função **AddPrinterDriver** instala um driver de impressora local ou remoto e associa a configuração, os dados e os arquivos de driver.</span><span class="sxs-lookup"><span data-stu-id="69d65-104">The **AddPrinterDriver** function installs a local or remote printer driver and associates the configuration, data, and driver files.</span></span>

<span data-ttu-id="69d65-105">Para obter mais flexibilidade na instalação ou atualização de drivers de impressora, use a função [**AddPrinterDriverEx**](addprinterdriverex.md) porque ela permite a atualização estrita, o downgrade estrito, a cópia somente de arquivos mais recentes e a cópia de todos os arquivos (independentemente dos carimbos de data/hora do arquivo).</span><span class="sxs-lookup"><span data-stu-id="69d65-105">For more flexibility in installing or upgrading printer drivers, use the [**AddPrinterDriverEx**](addprinterdriverex.md) function because it allows strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of the file time stamps).</span></span>

> [!Note]  
> <span data-ttu-id="69d65-106">A instalação de um driver de impressora sem um pacote de driver não é mais recomendada.</span><span class="sxs-lookup"><span data-stu-id="69d65-106">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="69d65-107">Use [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="69d65-107">Use [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) instead.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="69d65-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69d65-108">Syntax</span></span>


```C++
BOOL AddPrinterDriver(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pDriverInfo
);
```



## <a name="parameters"></a><span data-ttu-id="69d65-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69d65-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69d65-110">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69d65-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69d65-111">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual o driver deve ser instalado.</span><span class="sxs-lookup"><span data-stu-id="69d65-111">A pointer to a null-terminated string that specifies the name of the server on which the driver should be installed.</span></span>

<span data-ttu-id="69d65-112">Se *pname* for **nulo**, o driver será instalado localmente.</span><span class="sxs-lookup"><span data-stu-id="69d65-112">If *pName* is **NULL**, the driver will be installed locally.</span></span>

</dd> <dt>

<span data-ttu-id="69d65-113">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="69d65-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69d65-114">A versão da estrutura à qual o *pDriverInfo* aponta.</span><span class="sxs-lookup"><span data-stu-id="69d65-114">The version of the structure to which *pDriverInfo* points.</span></span>

<span data-ttu-id="69d65-115">Esse valor pode ser 2, 3, 4, 6 ou 8.</span><span class="sxs-lookup"><span data-stu-id="69d65-115">This value can be 2, 3, 4, 6, or 8.</span></span>

</dd> <dt>

<span data-ttu-id="69d65-116">*pDriverInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69d65-116">*pDriverInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69d65-117">Um ponteiro para uma estrutura que contém informações de driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="69d65-117">A pointer to a structure containing printer driver information.</span></span> <span data-ttu-id="69d65-118">Isso depende do valor do *nível*.</span><span class="sxs-lookup"><span data-stu-id="69d65-118">This depends on the value of *Level*.</span></span>



| <span data-ttu-id="69d65-119">Valor</span><span class="sxs-lookup"><span data-stu-id="69d65-119">Value</span></span> | <span data-ttu-id="69d65-120">Estrutura da unidade da impressora</span><span class="sxs-lookup"><span data-stu-id="69d65-120">Printer Drive Structure</span></span>                  |
|-------|------------------------------------------|
| <span data-ttu-id="69d65-121">2</span><span class="sxs-lookup"><span data-stu-id="69d65-121">2</span></span>     | [<span data-ttu-id="69d65-122">**Informações do DRIVER \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="69d65-122">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md) |
| <span data-ttu-id="69d65-123">3</span><span class="sxs-lookup"><span data-stu-id="69d65-123">3</span></span>     | [<span data-ttu-id="69d65-124">**Informações do DRIVER \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="69d65-124">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md) |
| <span data-ttu-id="69d65-125">4</span><span class="sxs-lookup"><span data-stu-id="69d65-125">4</span></span>     | [<span data-ttu-id="69d65-126">**Informações do DRIVER \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="69d65-126">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md) |
| <span data-ttu-id="69d65-127">6</span><span class="sxs-lookup"><span data-stu-id="69d65-127">6</span></span>     | [<span data-ttu-id="69d65-128">**Informações do DRIVER \_ \_ 6**</span><span class="sxs-lookup"><span data-stu-id="69d65-128">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md) |
| <span data-ttu-id="69d65-129">8</span><span class="sxs-lookup"><span data-stu-id="69d65-129">8</span></span>     | [<span data-ttu-id="69d65-130">**Informações do DRIVER \_ \_ 8**</span><span class="sxs-lookup"><span data-stu-id="69d65-130">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md) |



 

<span data-ttu-id="69d65-131">Se o membro **pEnvironment** da estrutura apontada por *pDriverInfo* for **NULL**, o ambiente atual do chamador/cliente (não do destino/servidor) será usado.</span><span class="sxs-lookup"><span data-stu-id="69d65-131">If the **pEnvironment** member of the structure pointed to by *pDriverInfo* is **NULL**, the current environment of the caller/client (not of the destination/server) is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69d65-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="69d65-132">Return value</span></span>

<span data-ttu-id="69d65-133">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="69d65-133">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="69d65-134">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="69d65-134">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="69d65-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="69d65-135">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="69d65-136">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="69d65-136">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="69d65-137">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="69d65-137">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="69d65-138">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="69d65-138">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="69d65-139">O chamador deve ter o [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="69d65-139">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="69d65-140">Antes que um aplicativo chame a função **AddPrinterDriver** , todos os arquivos exigidos pelo driver devem ser copiados para o diretório de driver de impressora do sistema.</span><span class="sxs-lookup"><span data-stu-id="69d65-140">Before an application calls the **AddPrinterDriver** function, all files required by the driver must be copied to the system's printer-driver directory.</span></span> <span data-ttu-id="69d65-141">Um aplicativo pode recuperar o nome desse diretório chamando a função [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="69d65-141">An application can retrieve the name of this directory by calling the [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) function.</span></span>

<span data-ttu-id="69d65-142">Um aplicativo pode determinar quais drivers de impressora estão instalados no momento chamando a função [**EnumPrinterDrivers**](enumprinterdrivers.md) .</span><span class="sxs-lookup"><span data-stu-id="69d65-142">An application can determine which printer drivers are currently installed by calling the [**EnumPrinterDrivers**](enumprinterdrivers.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="69d65-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69d65-143">Requirements</span></span>



| <span data-ttu-id="69d65-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="69d65-144">Requirement</span></span> | <span data-ttu-id="69d65-145">Valor</span><span class="sxs-lookup"><span data-stu-id="69d65-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69d65-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69d65-146">Minimum supported client</span></span><br/> | <span data-ttu-id="69d65-147">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="69d65-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="69d65-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69d65-148">Minimum supported server</span></span><br/> | <span data-ttu-id="69d65-149">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="69d65-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="69d65-150">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="69d65-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="69d65-151"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69d65-151"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="69d65-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="69d65-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="69d65-153"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69d65-153"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="69d65-154">DLL</span><span class="sxs-lookup"><span data-stu-id="69d65-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69d65-155"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="69d65-155"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="69d65-156">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="69d65-156">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="69d65-157">**AddPrinterDriverW** (Unicode) e **AddPrinterDriverA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="69d65-157">**AddPrinterDriverW** (Unicode) and **AddPrinterDriverA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="69d65-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="69d65-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69d65-159">Impressão</span><span class="sxs-lookup"><span data-stu-id="69d65-159">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="69d65-160">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="69d65-160">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="69d65-161">**AddPrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="69d65-161">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="69d65-162">**Informações do DRIVER \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="69d65-162">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="69d65-163">**Informações do DRIVER \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="69d65-163">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="69d65-164">**Informações do DRIVER \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="69d65-164">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="69d65-165">**Informações do DRIVER \_ \_ 6**</span><span class="sxs-lookup"><span data-stu-id="69d65-165">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="69d65-166">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="69d65-166">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="69d65-167">**GetPrinterDriverDirectory**</span><span class="sxs-lookup"><span data-stu-id="69d65-167">**GetPrinterDriverDirectory**</span></span>](getprinterdriverdirectory.md)
</dt> </dl>

 

