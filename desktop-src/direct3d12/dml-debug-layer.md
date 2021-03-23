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
# <a name="using-the-directml-debug-layer"></a>Usando a camada de depuração DirectML

A camada de depuração DirectML é um componente opcional de tempo de desenvolvimento que ajuda você a depurar seu código DirectML. A camada de depuração faz parte de um pacote de ferramentas gráficas separado, distribuído como um [recurso sob demanda](/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (fod). As ferramentas de gráficos FOD devem ser instaladas em seu sistema para que você possa usar a camada de depuração.

É altamente recomendável que você habilite a camada de depuração ao desenvolver aplicativos usando o DirectML, pois ele pode fornecer informações inestimávels no caso de uso inválido da API.

## <a name="installing-the-directml-debug-layer"></a>Instalando a camada de depuração DirectML

Para instalar o pacote de recurso de ferramentas gráficas opcionais (FOD), execute o seguinte comando em um prompt do PowerShell do administrador.

```powershell
Add-WindowsCapability -Online -Name "Tools.Graphics.DirectX~~~~0.0.1.0"
```

Como alternativa, você pode instalar o pacote de ferramentas de gráficos de dentro das configurações do Windows 10. Navegue até **configurações**  >  **aplicativos** aplicativo  >  **& recursos** recursos  >  **opcionais**  >  **Adicionar um recurso** >, em seguida, selecione **ferramentas de gráficos**.

## <a name="enabling-the-directml-debug-layer"></a>Habilitando a camada de depuração DirectML

Depois que o pacote de ferramentas de gráficos estiver instalado, você poderá habilitar a camada de depuração DirectML fornecendo  [**DML_CREATE_DEVICE_FLAG_DEBUG**](/windows/win32/api/directml/ne-directml-dml_create_device_flags) ao chamar [**DMLCreateDevice**](/windows/win32/api/directml/nf-directml-dmlcreatedevice).

> [!IMPORTANT]
> Você deve primeiro habilitar a camada de depuração do Direct3D 12. E *, em seguida,* habilite a camada de depuração DirectML chamando **DMLCreateDevice**.

Depois de habilitar a camada de depuração DirectML, quaisquer erros de DirectML ou chamadas de API inválidas farão com que as informações de depuração sejam emitidas como saída de depuração. Veja um exemplo.

```console
DML_OPERATOR_CONVOLUTION: invalid D3D12_HEAP_TYPE. DirectML requires all bound buffers to be D3D12_HEAP_TYPE_DEFAULT.
```

## <a name="see-also"></a>Confira também

* [Função DMLCreateDevice](/windows/win32/api/directml/nf-directml-dmlcreatedevice)
* [Recursos disponíveis-sob demanda](/windows-hardware/manufacture/desktop/features-on-demand-non-language-fod)
* [Usar a validação baseada em GPU com a camada de depuração do Direct3D 12](/windows/desktop/direct3d12/using-d3d12-debug-layer-gpu-based-validation)
* [Referência de camada de depuração do Direct3D 12](/windows/desktop/direct3d12/direct3d-12-sdklayers-reference)
