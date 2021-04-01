---
description: A função DocumentProperties recupera ou modifica informações de inicialização de impressora ou exibe uma folha de propriedades de configuração de impressora para a impressora especificada.
ms.assetid: e89a2f6f-2bac-4369-b526-f8e15028698b
title: Função DocumentProperties (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DocumentProperties
- DocumentPropertiesA
- DocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 732cb6901b444117d0599a2899327ebcb749cf74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091751"
---
# <a name="documentproperties-function"></a><span data-ttu-id="09bcc-103">Função DocumentProperties</span><span class="sxs-lookup"><span data-stu-id="09bcc-103">DocumentProperties function</span></span>

<span data-ttu-id="09bcc-104">A função **DocumentProperties** recupera ou modifica informações de inicialização de impressora ou exibe uma folha de propriedades de configuração de impressora para a impressora especificada.</span><span class="sxs-lookup"><span data-stu-id="09bcc-104">The **DocumentProperties** function retrieves or modifies printer initialization information or displays a printer-configuration property sheet for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="09bcc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09bcc-105">Syntax</span></span>


```C++
LONG DocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput,
  _In_  DWORD    fMode
);
```



## <a name="parameters"></a><span data-ttu-id="09bcc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09bcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09bcc-107">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09bcc-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09bcc-108">Um identificador para a janela pai da folha de propriedades de configuração da impressora.</span><span class="sxs-lookup"><span data-stu-id="09bcc-108">A handle to the parent window of the printer-configuration property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="09bcc-109">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09bcc-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09bcc-110">Um identificador para um objeto de impressora.</span><span class="sxs-lookup"><span data-stu-id="09bcc-110">A handle to a printer object.</span></span> <span data-ttu-id="09bcc-111">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="09bcc-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="09bcc-112">*pDeviceName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09bcc-112">*pDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09bcc-113">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do dispositivo para o qual a folha de propriedades de configuração de impressora é exibida.</span><span class="sxs-lookup"><span data-stu-id="09bcc-113">A pointer to a null-terminated string that specifies the name of the device for which the printer-configuration property sheet is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="09bcc-114">*pDevModeOutput* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="09bcc-114">*pDevModeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09bcc-115">Um ponteiro para uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que recebe os dados de configuração da impressora especificados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="09bcc-115">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that receives the printer configuration data specified by the user.</span></span>

</dd> <dt>

<span data-ttu-id="09bcc-116">*pDevModeInput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09bcc-116">*pDevModeInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09bcc-117">Um ponteiro para uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que o sistema operacional usa para inicializar os controles da folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="09bcc-117">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that the operating system uses to initialize the property sheet controls.</span></span>

<span data-ttu-id="09bcc-118">Esse parâmetro só será usado se o sinalizador **DM \_ in \_ buffer** estiver definido no parâmetro *fMode* .</span><span class="sxs-lookup"><span data-stu-id="09bcc-118">This parameter is only used if the **DM\_IN\_BUFFER** flag is set in the *fMode* parameter.</span></span> <span data-ttu-id="09bcc-119">Se o **DM \_ no \_ buffer** não estiver definido, o sistema operacional usará o [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)padrão da impressora.</span><span class="sxs-lookup"><span data-stu-id="09bcc-119">If **DM\_IN\_BUFFER** is not set, the operating system uses the printer's default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea).</span></span>

</dd> <dt>

<span data-ttu-id="09bcc-120">*fMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09bcc-120">*fMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09bcc-121">As operações que a função executa.</span><span class="sxs-lookup"><span data-stu-id="09bcc-121">The operations the function performs.</span></span> <span data-ttu-id="09bcc-122">Se esse parâmetro for zero, a função **DocumentProperties** retornará o número de bytes exigidos pela estrutura de dados [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) do driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="09bcc-122">If this parameter is zero, the **DocumentProperties** function returns the number of bytes required by the printer driver's [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) data structure.</span></span> <span data-ttu-id="09bcc-123">Caso contrário, use uma ou mais das seguintes constantes para construir um valor para esse parâmetro; no entanto, observe que, para alterar as configurações de impressão, um aplicativo deve especificar pelo menos um valor de entrada e um valor de saída.</span><span class="sxs-lookup"><span data-stu-id="09bcc-123">Otherwise, use one or more of the following constants to construct a value for this parameter; note, however, that in order to change the print settings, an application must specify at least one input value and one output value.</span></span>



| <span data-ttu-id="09bcc-124">Valor</span><span class="sxs-lookup"><span data-stu-id="09bcc-124">Value</span></span>                                                                                                                                                          | <span data-ttu-id="09bcc-125">Significado</span><span class="sxs-lookup"><span data-stu-id="09bcc-125">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DM_IN_BUFFER"></span><span id="dm_in_buffer"></span><dl> <span data-ttu-id="09bcc-126"><dt>**DM \_ no \_ buffer**</dt></span><span class="sxs-lookup"><span data-stu-id="09bcc-126"><dt>**DM\_IN\_BUFFER**</dt></span></span> </dl>    | <span data-ttu-id="09bcc-127">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="09bcc-127">Input value.</span></span> <span data-ttu-id="09bcc-128">Antes de solicitar, copiar ou atualizar, a função mescla as configurações de impressão atuais do driver de impressora com as configurações na estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) especificada pelo parâmetro *pDevModeInput* .</span><span class="sxs-lookup"><span data-stu-id="09bcc-128">Before prompting, copying, or updating, the function merges the printer driver's current print settings with the settings in the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure specified by the *pDevModeInput* parameter.</span></span> <span data-ttu-id="09bcc-129">A função atualiza a estrutura somente para os membros especificados pelo membro **dmFields** da estrutura **DEVMODE** .</span><span class="sxs-lookup"><span data-stu-id="09bcc-129">The function updates the structure only for those members specified by the **DEVMODE** structure's **dmFields** member.</span></span> <span data-ttu-id="09bcc-130">Esse valor também é definido como **DM \_ Modify**.</span><span class="sxs-lookup"><span data-stu-id="09bcc-130">This value is also defined as **DM\_MODIFY**.</span></span> <span data-ttu-id="09bcc-131">Em casos de conflito durante a mesclagem, as configurações na estrutura **DEVMODE** especificada por *pDevModeInput* substituem as configurações de impressão atuais do driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="09bcc-131">In cases of conflict during the merge, the settings in the **DEVMODE** structure specified by *pDevModeInput* override the printer driver's current print settings.</span></span><br/> |
| <span id="DM_IN_PROMPT"></span><span id="dm_in_prompt"></span><dl> <span data-ttu-id="09bcc-132"><dt>**DM \_ no \_ prompt**</dt></span><span class="sxs-lookup"><span data-stu-id="09bcc-132"><dt>**DM\_IN\_PROMPT**</dt></span></span> </dl>    | <span data-ttu-id="09bcc-133">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="09bcc-133">Input value.</span></span> <span data-ttu-id="09bcc-134">A função apresenta a folha de propriedades de configuração de impressão do driver de impressora e, em seguida, altera as configurações na estrutura de dados [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) da impressora para esses valores especificados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="09bcc-134">The function presents the printer driver's Print Setup property sheet and then changes the settings in the printer's [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) data structure to those values specified by the user.</span></span> <span data-ttu-id="09bcc-135">Esse valor também é definido como **\_ prompt DM**.</span><span class="sxs-lookup"><span data-stu-id="09bcc-135">This value is also defined as **DM\_PROMPT**.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="DM_OUT_BUFFER"></span><span id="dm_out_buffer"></span><dl> <span data-ttu-id="09bcc-136"><dt>**\_buffer de saída DM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="09bcc-136"><dt>**DM\_OUT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="09bcc-137">Valor de saída.</span><span class="sxs-lookup"><span data-stu-id="09bcc-137">Output value.</span></span> <span data-ttu-id="09bcc-138">A função grava as configurações de impressão atuais do driver de impressora, incluindo dados privados, na estrutura de dados [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) especificada pelo parâmetro *pDevModeOutput* .</span><span class="sxs-lookup"><span data-stu-id="09bcc-138">The function writes the printer driver's current print settings, including private data, to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) data structure specified by the *pDevModeOutput* parameter.</span></span> <span data-ttu-id="09bcc-139">O chamador deve alocar um buffer suficientemente grande para conter as informações.</span><span class="sxs-lookup"><span data-stu-id="09bcc-139">The caller must allocate a buffer sufficiently large to contain the information.</span></span> <span data-ttu-id="09bcc-140">Se os conjuntos **de \_ \_ buffers de saída** de bit DM estiverem claros, o parâmetro *pDevModeOutput* poderá ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="09bcc-140">If the bit **DM\_OUT\_BUFFER** sets is clear, the *pDevModeOutput* parameter can be **NULL**.</span></span> <span data-ttu-id="09bcc-141">Esse valor também é definido como **\_ cópia DM**.</span><span class="sxs-lookup"><span data-stu-id="09bcc-141">This value is also defined as **DM\_COPY**.</span></span><br/>                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09bcc-142">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="09bcc-142">Return value</span></span>

<span data-ttu-id="09bcc-143">Se o parâmetro *fMode* for zero, o valor de retorno será o tamanho do buffer necessário para conter os dados de inicialização do driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="09bcc-143">If the *fMode* parameter is zero, the return value is the size of the buffer required to contain the printer driver initialization data.</span></span> <span data-ttu-id="09bcc-144">Observe que esse buffer pode ser maior do que uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) se o driver de impressora acrescentar dados privados à estrutura.</span><span class="sxs-lookup"><span data-stu-id="09bcc-144">Note that this buffer can be larger than a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure if the printer driver appends private data to the structure.</span></span>

<span data-ttu-id="09bcc-145">Se a função exibir a folha de propriedades, o valor de retorno será **IDOK** ou **IDCANCEL**, dependendo de qual botão o usuário selecionar.</span><span class="sxs-lookup"><span data-stu-id="09bcc-145">If the function displays the property sheet, the return value is either **IDOK** or **IDCANCEL**, depending on which button the user selects.</span></span>

<span data-ttu-id="09bcc-146">Se a função não exibir a folha de propriedades e for bem-sucedida, o valor de retorno será **IDOK**.</span><span class="sxs-lookup"><span data-stu-id="09bcc-146">If the function does not display the property sheet and is successful, the return value is **IDOK**.</span></span>

<span data-ttu-id="09bcc-147">Se a função falhar, o valor de retorno será menor que zero.</span><span class="sxs-lookup"><span data-stu-id="09bcc-147">If the function fails, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="09bcc-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="09bcc-148">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="09bcc-149">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="09bcc-149">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="09bcc-150">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="09bcc-150">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="09bcc-151">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="09bcc-151">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="09bcc-152">A cadeia de caracteres apontada pelo parâmetro *pDeviceName* pode ser obtida chamando-se a função [**getprintr**](getprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="09bcc-152">The string pointed to by the *pDeviceName* parameter can be obtained by calling the [**GetPrinter**](getprinter.md) function.</span></span>

<span data-ttu-id="09bcc-153">A estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) realmente usada por um driver de impressora contém a parte independente do dispositivo (conforme definido acima) seguida por uma parte específica do driver que varia em tamanho e conteúdo com cada driver e versão de driver.</span><span class="sxs-lookup"><span data-stu-id="09bcc-153">The [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure actually used by a printer driver contains the device-independent part (as defined above) followed by a driver-specific part that varies in size and content with each driver and driver version.</span></span> <span data-ttu-id="09bcc-154">Devido a essa dependência de driver, é muito importante que os aplicativos consultem o driver para obter o tamanho correto da estrutura **DEVMODE** antes de alocar um buffer para ele.</span><span class="sxs-lookup"><span data-stu-id="09bcc-154">Because of this driver dependence, it is very important for applications to query the driver for the correct size of the **DEVMODE** structure before allocating a buffer for it.</span></span>

<span data-ttu-id="09bcc-155">**Para fazer alterações nas configurações de impressão locais de um aplicativo, um aplicativo deve seguir estas etapas:**</span><span class="sxs-lookup"><span data-stu-id="09bcc-155">**To make changes to print settings that are local to an application, an application should follow these steps:**</span></span>

1.  <span data-ttu-id="09bcc-156">Obtenha o número de bytes necessários para a estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) completa chamando **DocumentProperties** e especificando zero no parâmetro *fMode* .</span><span class="sxs-lookup"><span data-stu-id="09bcc-156">Get the number of bytes required for the full [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure by calling **DocumentProperties** and specifying zero in the *fMode* parameter.</span></span>
2.  <span data-ttu-id="09bcc-157">Aloque memória para a estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) completa.</span><span class="sxs-lookup"><span data-stu-id="09bcc-157">Allocate memory for the full [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>
3.  <span data-ttu-id="09bcc-158">Obtenha as configurações atuais da impressora chamando **DocumentProperties**.</span><span class="sxs-lookup"><span data-stu-id="09bcc-158">Get the current printer settings by calling **DocumentProperties**.</span></span> <span data-ttu-id="09bcc-159">Passe um ponteiro para a estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) alocada na etapa 2 como o parâmetro *pDevModeOutput* e especifique o valor do **\_ \_ buffer de saída DM** .</span><span class="sxs-lookup"><span data-stu-id="09bcc-159">Pass a pointer to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure allocated in Step 2 as the *pDevModeOutput* parameter and specify the **DM\_OUT\_BUFFER** value.</span></span>
4.  <span data-ttu-id="09bcc-160">Modifique os membros apropriados da estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) retornada e indique quais membros foram alterados definindo os bits correspondentes no membro **dmFields** do **DEVMODE**.</span><span class="sxs-lookup"><span data-stu-id="09bcc-160">Modify the appropriate members of the returned [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure and indicate which members were changed by setting the corresponding bits in the **dmFields** member of the **DEVMODE**.</span></span>
5.  <span data-ttu-id="09bcc-161">Chame **DocumentProperties** e passe a estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) modificada de volta como os parâmetros *pDevModeInput* e *PDevModeOutput* e especifique os valores de buffer **DM \_ no \_ buffer** e **DM \_ out \_** (que são combinados usando o operador OR). A estrutura **DEVMODE** retornada pela terceira chamada para **DocumentProperties** pode ser usada como um argumento em uma chamada para a função [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) .</span><span class="sxs-lookup"><span data-stu-id="09bcc-161">Call **DocumentProperties** and pass the modified [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure back as both the *pDevModeInput* and *pDevModeOutput* parameters and specify both the **DM\_IN\_BUFFER** and **DM\_OUT\_BUFFER** values (which are combined using the OR operator).The **DEVMODE** structure returned by the third call to **DocumentProperties** can be used as an argument in a call to the [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) function.</span></span>

<span data-ttu-id="09bcc-162">Para criar um identificador para um contexto de dispositivo de impressora usando as configurações de impressora atuais, você só precisa chamar **DocumentProperties** duas vezes, conforme descrito acima.</span><span class="sxs-lookup"><span data-stu-id="09bcc-162">To create a handle to a printer-device context using the current printer settings, you only need to call **DocumentProperties** twice, as described above.</span></span> <span data-ttu-id="09bcc-163">A primeira chamada Obtém o tamanho do [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) completo e a segunda chamada Inicializa o **DEVMODE** com as configurações de impressora atuais.</span><span class="sxs-lookup"><span data-stu-id="09bcc-163">The first call gets the size of the full [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) and the second call initializes the **DEVMODE** with the current printer settings.</span></span> <span data-ttu-id="09bcc-164">Passe o **DEVMODE** inicializado para [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) para obter o identificador para o contexto do dispositivo de impressora.</span><span class="sxs-lookup"><span data-stu-id="09bcc-164">Pass the initialized **DEVMODE** to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) to obtain the handle to the printer device context.</span></span>

## <a name="requirements"></a><span data-ttu-id="09bcc-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09bcc-165">Requirements</span></span>



| <span data-ttu-id="09bcc-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="09bcc-166">Requirement</span></span> | <span data-ttu-id="09bcc-167">Valor</span><span class="sxs-lookup"><span data-stu-id="09bcc-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09bcc-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09bcc-168">Minimum supported client</span></span><br/> | <span data-ttu-id="09bcc-169">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="09bcc-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="09bcc-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09bcc-170">Minimum supported server</span></span><br/> | <span data-ttu-id="09bcc-171">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="09bcc-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="09bcc-172">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="09bcc-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="09bcc-173"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09bcc-173"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="09bcc-174">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="09bcc-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="09bcc-175"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09bcc-175"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="09bcc-176">DLL</span><span class="sxs-lookup"><span data-stu-id="09bcc-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09bcc-177"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="09bcc-177"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="09bcc-178">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="09bcc-178">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="09bcc-179">**DocumentPropertiesW** (Unicode) e **DocumentPropertiesA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="09bcc-179">**DocumentPropertiesW** (Unicode) and **DocumentPropertiesA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="09bcc-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="09bcc-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09bcc-181">Impressão</span><span class="sxs-lookup"><span data-stu-id="09bcc-181">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="09bcc-182">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="09bcc-182">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="09bcc-183">**AdvancedDocumentProperties**</span><span class="sxs-lookup"><span data-stu-id="09bcc-183">**AdvancedDocumentProperties**</span></span>](advanceddocumentproperties.md)
</dt> <dt>

[<span data-ttu-id="09bcc-184">**CreateDC**</span><span class="sxs-lookup"><span data-stu-id="09bcc-184">**CreateDC**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-createdca)
</dt> <dt>

[<span data-ttu-id="09bcc-185">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="09bcc-185">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="09bcc-186">**Getprinter**</span><span class="sxs-lookup"><span data-stu-id="09bcc-186">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="09bcc-187">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="09bcc-187">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

