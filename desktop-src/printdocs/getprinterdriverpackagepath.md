---
description: Recupera o caminho para o pacote de driver de impressora especificado em um servidor de impressão.
ms.assetid: e88e984b-d2c0-43b4-8f70-b05ec202ab14
title: Função GetPrinterDriverPackagePath (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverPackagePath
- GetPrinterDriverPackagePathA
- GetPrinterDriverPackagePathW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ea355782df6cce7910f92a46af3cde320536106e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785104"
---
# <a name="getprinterdriverpackagepath-function"></a><span data-ttu-id="e6547-103">Função GetPrinterDriverPackagePath</span><span class="sxs-lookup"><span data-stu-id="e6547-103">GetPrinterDriverPackagePath function</span></span>

<span data-ttu-id="e6547-104">Recupera o caminho para o pacote de driver de impressora especificado em um servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="e6547-104">Retrieves the path to the specified printer driver package on a print server.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6547-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6547-105">Syntax</span></span>


```C++
HRESULT GetPrinterDriverPackagePath(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszEnvironment,
  _In_    LPCTSTR pszLanguage,
  _In_    LPCTSTR pszPackageID,
  _Inout_ LPTSTR  pszDriverPackageCab,
  _In_    DWORD   cchDriverPackageCab,
  _Out_   LPDWORD pcchRequiredSize
);
```



## <a name="parameters"></a><span data-ttu-id="e6547-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6547-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6547-107">*pszServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6547-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6547-108">Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica o nome do servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="e6547-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="e6547-109">Use **NULL** para o computador local.</span><span class="sxs-lookup"><span data-stu-id="e6547-109">Use **NULL** for the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="e6547-110">*pszEnvironment* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6547-110">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6547-111">Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica a arquitetura do processador (por exemplo, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="e6547-111">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="e6547-112">Isso pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e6547-112">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e6547-113">*pszLanguage* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6547-113">*pszLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6547-114">Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica o idioma da [interface do usuário multilíngüe](/windows/desktop/Intl/mui-resource-management) para o driver que está sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="e6547-114">A pointer to a constant, null-terminated string that specifies the [Multilingual User Interface](/windows/desktop/Intl/mui-resource-management) language for the driver being installed.</span></span> <span data-ttu-id="e6547-115">Isso pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e6547-115">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e6547-116">*pszPackageID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6547-116">*pszPackageID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6547-117">Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica a ID do pacote de driver.</span><span class="sxs-lookup"><span data-stu-id="e6547-117">A pointer to a constant, null-terminated string that specifies the ID of the driver package.</span></span>

</dd> <dt>

<span data-ttu-id="e6547-118">*pszDriverPackageCab* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e6547-118">*pszDriverPackageCab* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6547-119">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o caminho para o arquivo de gabinete para o pacote de driver.</span><span class="sxs-lookup"><span data-stu-id="e6547-119">A pointer to a null-terminated string that specifies the path to the cabinet file for the driver package.</span></span> <span data-ttu-id="e6547-120">Isso pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e6547-120">This can be **NULL**.</span></span> <span data-ttu-id="e6547-121">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="e6547-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e6547-122">*cchDriverPackageCab* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6547-122">*cchDriverPackageCab* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6547-123">O tamanho, em caracteres, do buffer *pszDriverPackageCab* .</span><span class="sxs-lookup"><span data-stu-id="e6547-123">The size, in characters, of the *pszDriverPackageCab* buffer.</span></span> <span data-ttu-id="e6547-124">Isso pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e6547-124">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e6547-125">*pcchRequiredSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e6547-125">*pcchRequiredSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6547-126">Um ponteiro para o tamanho necessário do buffer *pszDriverPackageCab* .</span><span class="sxs-lookup"><span data-stu-id="e6547-126">A pointer to the required size of the *pszDriverPackageCab* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6547-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e6547-127">Return value</span></span>

<span data-ttu-id="e6547-128">Se a operação for concluída com sucesso, o valor de retorno será S \_ OK, caso contrário, o **HRESULT** conterá um código de erro.</span><span class="sxs-lookup"><span data-stu-id="e6547-128">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="e6547-129">Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="e6547-129">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e6547-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6547-130">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e6547-131">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="e6547-131">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e6547-132">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e6547-132">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e6547-133">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="e6547-133">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="e6547-134">Para obter um valor para *cchDriverPackageCab*, chame a função com **NULL** como o valor de *pszDriverPackageCab*.</span><span class="sxs-lookup"><span data-stu-id="e6547-134">To obtain a value for *cchDriverPackageCab*, call the function with **NULL** as the value of *pszDriverPackageCab*.</span></span> <span data-ttu-id="e6547-135">Use o valor retornado em *pcchRequiredSize* como o valor de *cchDriverPackageCab* e chame a função novamente.</span><span class="sxs-lookup"><span data-stu-id="e6547-135">Use the value returned in *pcchRequiredSize* as the value of *cchDriverPackageCab* and call the function again.</span></span>

<span data-ttu-id="e6547-136">O *pszPackageID* normalmente é obtido de uma chamada para [**GetCorePrinterDrivers**](getcoreprinterdrivers.md).</span><span class="sxs-lookup"><span data-stu-id="e6547-136">The *pszPackageID* is typically obtained from a call to [**GetCorePrinterDrivers**](getcoreprinterdrivers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6547-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6547-137">Requirements</span></span>



| <span data-ttu-id="e6547-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6547-138">Requirement</span></span> | <span data-ttu-id="e6547-139">Valor</span><span class="sxs-lookup"><span data-stu-id="e6547-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6547-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6547-140">Minimum supported client</span></span><br/> | <span data-ttu-id="e6547-141">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6547-141">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e6547-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6547-142">Minimum supported server</span></span><br/> | <span data-ttu-id="e6547-143">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e6547-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e6547-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e6547-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6547-145"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6547-145"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e6547-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6547-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="e6547-147"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6547-147"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e6547-148">DLL</span><span class="sxs-lookup"><span data-stu-id="e6547-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6547-149"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6547-149"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="e6547-150">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e6547-150">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e6547-151">**GetPrinterDriverPackagePathW** (Unicode) e **GetPrinterDriverPackagePathA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e6547-151">**GetPrinterDriverPackagePathW** (Unicode) and **GetPrinterDriverPackagePathA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="e6547-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6547-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6547-153">Impressão</span><span class="sxs-lookup"><span data-stu-id="e6547-153">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e6547-154">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="e6547-154">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

