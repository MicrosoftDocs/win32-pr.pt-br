---
title: Usando a camada de depuração DirectML
description: A camada de depuração DirectML é um componente opcional de tempo de desenvolvimento que ajuda você a depurar seu código DirectML.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: f885595e5cc3b3890d208875fb92e47e0dc5e337
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104548253"
---
# <a name="using-the-directml-debug-layer"></a><span data-ttu-id="42b0d-103">Usando a camada de depuração DirectML</span><span class="sxs-lookup"><span data-stu-id="42b0d-103">Using the DirectML debug layer</span></span>

<span data-ttu-id="42b0d-104">A camada de depuração DirectML é um componente opcional de tempo de desenvolvimento que ajuda você a depurar seu código DirectML.</span><span class="sxs-lookup"><span data-stu-id="42b0d-104">The DirectML debug layer is an optional development-time component that helps you in debugging your DirectML code.</span></span> <span data-ttu-id="42b0d-105">A camada de depuração faz parte de um pacote de ferramentas gráficas separado, distribuído como um [recurso sob demanda](/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (fod).</span><span class="sxs-lookup"><span data-stu-id="42b0d-105">The debug layer is part of a separate Graphics Tools package, distributed as a [Feature-on-Demand](/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (FOD).</span></span> <span data-ttu-id="42b0d-106">As ferramentas de gráficos FOD devem ser instaladas em seu sistema para que você possa usar a camada de depuração.</span><span class="sxs-lookup"><span data-stu-id="42b0d-106">The Graphics Tools FOD must be installed on your system in order to use the debug layer.</span></span>

<span data-ttu-id="42b0d-107">É altamente recomendável que você habilite a camada de depuração ao desenvolver aplicativos usando o DirectML, pois ele pode fornecer informações inestimávels no caso de uso inválido da API.</span><span class="sxs-lookup"><span data-stu-id="42b0d-107">We highly recommended that you enable the debug layer while developing applications using DirectML, because it can provide invaluable information in the event of invalid API usage.</span></span>

## <a name="installing-the-directml-debug-layer"></a><span data-ttu-id="42b0d-108">Instalando a camada de depuração DirectML</span><span class="sxs-lookup"><span data-stu-id="42b0d-108">Installing the DirectML debug layer</span></span>

<span data-ttu-id="42b0d-109">Para instalar o pacote de recurso de ferramentas gráficas opcionais (FOD), execute o seguinte comando em um prompt do PowerShell do administrador.</span><span class="sxs-lookup"><span data-stu-id="42b0d-109">To install the optional Graphics Tools feature-on-demand (FOD) package, run the following command from an administrator Powershell prompt.</span></span>

```powershell
Add-WindowsCapability -Online -Name "Tools.Graphics.DirectX~~~~0.0.1.0"
```

<span data-ttu-id="42b0d-110">Como alternativa, você pode instalar o pacote de ferramentas de gráficos de dentro das configurações do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="42b0d-110">Alternatively, you can install the Graphics Tools package from within Windows 10 Settings.</span></span> <span data-ttu-id="42b0d-111">Navegue até **configurações**  >  **aplicativos** aplicativo  >  **& recursos** recursos  >  **opcionais**  >  **Adicionar um recurso** >, em seguida, selecione **ferramentas de gráficos**.</span><span class="sxs-lookup"><span data-stu-id="42b0d-111">Navigate to **Settings** > **Apps** > **Apps & features** > **Optional features** > **Add a feature** > then select **Graphics Tools**.</span></span>

## <a name="enabling-the-directml-debug-layer"></a><span data-ttu-id="42b0d-112">Habilitando a camada de depuração DirectML</span><span class="sxs-lookup"><span data-stu-id="42b0d-112">Enabling the DirectML debug layer</span></span>

<span data-ttu-id="42b0d-113">Depois que o pacote de ferramentas de gráficos estiver instalado, você poderá habilitar a camada de depuração DirectML fornecendo  [**DML_CREATE_DEVICE_FLAG_DEBUG**](/windows/win32/api/directml/ne-directml-dml_create_device_flags) ao chamar [**DMLCreateDevice**](/windows/win32/api/directml/nf-directml-dmlcreatedevice).</span><span class="sxs-lookup"><span data-stu-id="42b0d-113">Once the Graphics Tools package is installed, you can enable the DirectML debug layer by supplying  [**DML_CREATE_DEVICE_FLAG_DEBUG**](/windows/win32/api/directml/ne-directml-dml_create_device_flags) when you call [**DMLCreateDevice**](/windows/win32/api/directml/nf-directml-dmlcreatedevice).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="42b0d-114">Você deve primeiro habilitar a camada de depuração do Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="42b0d-114">You must first enable the Direct3D 12 debug layer.</span></span> <span data-ttu-id="42b0d-115">E *, em seguida,* habilite a camada de depuração DirectML chamando **DMLCreateDevice**.</span><span class="sxs-lookup"><span data-stu-id="42b0d-115">And *then* enable the DirectML debug layer by calling **DMLCreateDevice**.</span></span>

<span data-ttu-id="42b0d-116">Depois de habilitar a camada de depuração DirectML, quaisquer erros de DirectML ou chamadas de API inválidas farão com que as informações de depuração sejam emitidas como saída de depuração.</span><span class="sxs-lookup"><span data-stu-id="42b0d-116">Once you've enabled the DirectML debug layer, any DirectML errors or invalid API calls will cause debugging information to be emitted as debug output.</span></span> <span data-ttu-id="42b0d-117">Veja um exemplo.</span><span class="sxs-lookup"><span data-stu-id="42b0d-117">Here's an example.</span></span>

```console
DML_OPERATOR_CONVOLUTION: invalid D3D12_HEAP_TYPE. DirectML requires all bound buffers to be D3D12_HEAP_TYPE_DEFAULT.
```

## <a name="see-also"></a><span data-ttu-id="42b0d-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="42b0d-118">See also</span></span>

* [<span data-ttu-id="42b0d-119">Função DMLCreateDevice</span><span class="sxs-lookup"><span data-stu-id="42b0d-119">DMLCreateDevice function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice)
* [<span data-ttu-id="42b0d-120">Recursos disponíveis-sob demanda</span><span class="sxs-lookup"><span data-stu-id="42b0d-120">Available Features-on-Demand</span></span>](/windows-hardware/manufacture/desktop/features-on-demand-non-language-fod)
* [<span data-ttu-id="42b0d-121">Usar a validação baseada em GPU com a camada de depuração do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="42b0d-121">Use GPU-based validation with the Direct3D 12 Debug Layer</span></span>](/windows/desktop/direct3d12/using-d3d12-debug-layer-gpu-based-validation)
* [<span data-ttu-id="42b0d-122">Referência de camada de depuração do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="42b0d-122">Direct3D 12 Debug Layer reference</span></span>](/windows/desktop/direct3d12/direct3d-12-sdklayers-reference)
