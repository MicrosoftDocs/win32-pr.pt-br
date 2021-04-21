---
UID: NF:directml.DMLCreateDevice1
title: Função DMLCreateDevice1
description: Cria um dispositivo DirectML para um determinado dispositivo Direct3D 12.
helpviewer_keywords:
- DMLCreateDevice1
- DMLCreateDevice1 function
- direct3d12.dmlcreatedevice1
- directml/DMLCreateDevice1
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DMLCreateDevice1
- directml/DMLCreateDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- DirectML.dll
api_name:
- DMLCreateDevice1
ms.openlocfilehash: f722b12208bd808f01e177feb907f94c33541496
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803765"
---
# <a name="dmlcreatedevice1-function-directmlh"></a>Função DMLCreateDevice1 (directml. h)

Cria um dispositivo DirectML para um determinado dispositivo Direct3D 12.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior. Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxe

```cpp
HRESULT DMLCreateDevice1(
  ID3D12Device            *d3d12Device,
  DML_CREATE_DEVICE_FLAGS flags,
  DML_FEATURE_LEVEL       minimumFeatureLevel,
  REFIID                  riid,
  void                    **ppv
);
```

## <a name="parameters"></a>Parâmetros

`d3d12Device`

Tipo: <b> <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>*</b>

Um ponteiro para um [ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) que representa o dispositivo Direct3D 12 para criar o dispositivo DirectML. O DirectML dá suporte a qualquer nível de recurso do D3D e a dispositivos Direct3D 12 criados em qualquer adaptador, incluindo WARPing. No entanto, nem todos os recursos do DirectML podem estar disponíveis dependendo dos recursos do dispositivo Direct3D 12. Consulte [IDMLDevice:: CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport) para obter mais informações.

Se a chamada para **DMLCreateDevice1** for bem-sucedida, o dispositivo DirectML manterá uma referência forte para o dispositivo Direct3D 12 fornecido.

`flags`

Tipo: <b>DML_CREATE_DEVICE_FLAGS</b>

Um valor [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) especificando opções de criação de dispositivo adicionais.

`minimumFeatureLevel`

Tipo: <b>DML_FEATURE_LEVEL</b>

Um valor [DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) especificando o suporte mínimo de nível de recurso necessário.

Esse parâmetro pode ser útil para chamadores que exigem uma versão específica do DirectML, mas que podem se chamar em uma versão mais antiga do DirectML. Isso pode acontecer, por exemplo, quando o usuário executa seu aplicativo em uma versão mais antiga do Windows 10.

Os aplicativos que dependem explicitamente da funcionalidade introduzida em um nível de recurso específico podem especificá-lo como um *minimumFeatureLevel*. Isso garantirá que o **DMLCreateDevice1** não terá sucesso, a menos que a implementação subjacente seja *pelo menos* compatível com o nível de recurso mínimo solicitado.

Observe que, como esse parâmetro especifica um nível de recurso *mínimo* , o dispositivo DirectML subjacente pode, na verdade, dar suporte a um nível de recurso mais alto do que o mínimo solicitado. Depois que a criação do dispositivo for realizada com sucesso, você poderá consultar todos os níveis de recurso com suporte neste dispositivo usando [IDMLDevice:: CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport).

`riid`

Tipo: <b>REFIID</b>

Uma referência ao GUID (identificador global exclusivo) da interface que você deseja retornar no <i>dispositivo</i>. Espera-se que seja o GUID de [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).

`ppv`

Tipo: \_ com \_ Outptr \_ opt \_ <b>void * *</b>

Um ponteiro para um bloco de memória que recebe um ponteiro para o dispositivo. Esse é o endereço de um ponteiro para um [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice), representando o dispositivo DirectML criado.


## <a name="return-value"></a>Retornar valor

Tipo: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)

Se a função for realizada com sucesso, ela retornará <b>S_OK</b>. Caso contrário, ele retorna um código de erro [HRESULT](/windows/desktop/winprog/windows-data-types) .

Se esta versão do DirectML não oferecer suporte ao *minimumFeatureLevel* solicitado, essa função retornará **DXGI_ERROR_UNSUPPORTED**.

O FOD (recurso de ferramentas de gráficos sob demanda) deve ser instalado para usar as camadas de depuração do DirectML. Se o sinalizador de [DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags) for especificado em *flags* e as camadas de depuração não estiverem instaladas, **DMLCreateDevice1** retornará **DXGI_ERROR_SDK_COMPONENT_MISSING**.

## <a name="remarks"></a>Comentários

Uma versão mais recente dessa função, [DMLCreateDevice1](), foi introduzida no DirectML versão 1.1.0. **DMLCreateDevice1** é equivalente a chamar **DMLCreateDevice1** e fornecer um *minimumFeatureLevel* de [DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level).

## <a name="availability"></a>Disponibilidade

Essa API foi introduzida na versão DirectML `1.1.0` .

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de Destino** | Windows |
| **Cabeçalho** | directml. h |
| **Biblioteca** | DirectML. lib |
| **DLL** | DirectML.dll |

## <a name="see-also"></a>Confira também

* [Enumeração de DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [Histórico de versão do DirectML](../dml-version-history.md)
* [Histórico do nível de recurso do DirectML](/windows/win32/direct3d12/dml-feature_level-history)    
* [Usando a camada de depuração DirectML](../dml-debug-layer.md)