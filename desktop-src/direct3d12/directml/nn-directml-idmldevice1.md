---
UID: NN:directml.IDMLDevice1
title: IDMLDevice1
description: Representa um dispositivo DirectML, que é usado para criar operadores, tabelas de associação, gravadores de comandos e outros objetos.
helpviewer_keywords:
- IDMLDevice1
- IDMLDevice1 interface
- IDMLDevice1 interface
- described
- direct3d12.idmldevice1
- directml/IDMLDevice1
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
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1
- directml/IDMLDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.h
api_name:
- IDMLDevice1
ms.openlocfilehash: 7a10cf2c9fe683775d163c7b5cb0e30fe07de08f
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416919"
---
# <a name="idmldevice1-interface-directmlh"></a>Interface IDMLDevice1 (directml. h)

Representa um dispositivo DirectML, que é usado para criar operadores, tabelas de associação, gravadores de comandos e outros objetos. A interface **IDMLDevice1** herda de [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).

Um dispositivo DirectML sempre está associado a exatamente um dispositivo Direct3D 12 subjacente. Todos os objetos criados pelo dispositivo DirectML mantêm uma referência forte para seu dispositivo pai. Ao contrário do dispositivo Direct3D 12, o dispositivo DML não é um singleton. Portanto, é possível criar vários dispositivos DirectML no mesmo dispositivo Direct3D 12. No entanto, isso não é recomendado, pois o dispositivo DirectML não tem um estado mutável, portanto, há pouca vantagem em criar vários dispositivos DML no mesmo dispositivo Direct3D 12.

Esse objeto é thread-safe.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior. Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="availability"></a>Disponibilidade
Essa API foi introduzida na versão DirectML `1.1.0` .

## <a name="tensor-constraints"></a>Restrições de tensor
**Plataforma de destino**: Windows


## <a name="inheritance"></a>Herança


A interface IDMLDevice1 herda da interface IDMLDevice.



## <a name="methods"></a>Métodos

<p>A interface <b>IDMLDevice1</b> tem esses métodos.</p>

| Método | Descrição |
| ---- |:---- |
| [IDMLDevice1::CompileGraph](../directml/nf-directml-idmldevice1-compilegraph.md) | Compila um grafo de operadores DirectML em um objeto que pode ser expedido para a GPU. |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de Destino** | Windows |
| **Cabeçalho** | directml. h |

## <a name="see-also"></a>Confira também

[Interface IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice)