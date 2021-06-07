---
title: Interfaces do DirectML
description: As interfaces a seguir são declaradas em DirectML. h.
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 64ae11c5b9a4298c340488499a5a309b71a2d48b
ms.sourcegitcommit: d168355cd7112871f24643b4079c2640b36f4975
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/05/2021
ms.locfileid: "111521169"
---
# <a name="directml-interfaces"></a>Interfaces do DirectML

As interfaces a seguir são declaradas em DirectML. h.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [**IDMLBindingTable**](/windows/desktop/api/directml/nn-directml-idmlbindingtable) | Cria um dispositivo DirectML para um determinado dispositivo Direct3D 12. |
| [**IDMLCommandRecorder**](/windows/desktop/api/directml/nn-directml-idmlcommandrecorder) | Registra expedis of DirectML work em uma lista de comandos do Direct3D 12. |
| [**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) | Representa uma forma compilada e eficiente de um operador adequado para execução na GPU. |
| [**IDMLDebugDevice**](/windows/desktop/api/directml/nn-directml-idmldebugdevice) | Controla a camada de depuração DirectML. |
| [**IDMLDevice**](/windows/desktop/api/directml/nn-directml-idmldevice) | Representa um dispositivo DirectML, que é usado para criar operadores, tabelas de associação, gravadores de comandos e outros objetos. |
| [**IDMLDevice1**](/windows/desktop/api/directml/nn-directml-idmldevice1) | Representa um dispositivo DirectML, que é usado para criar operadores, tabelas de associação, gravadores de comandos e outros objetos. |
| [**IDMLDeviceChild**](/windows/win32/api/directml/nn-directml-idmldevicechild) | Uma interface implementada por todos os objetos criados a partir do dispositivo DirectML. |
| [**IDMLDispatchable**](/windows/desktop/api/directml/nn-directml-idmldispatchable) | Implementado por objetos que podem ser registrados em uma lista de comandos para expedição na GPU, usando [IDMLCommandRecorder:: RecordDispatch](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch). |
| [**IDMLObject**](/windows/desktop/api/directml/nn-directml-idmlobject) | Uma interface da qual [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice) e [IDMLDeviceChild](/windows/desktop/api/directml/nn-directml-idmldevicechild) herdam diretamente (e todas as outras interfaces indiretamente). Consequentemente, ele fornece métodos comuns a todas as interfaces DirectML, especificamente métodos para associar dados privados e anotar nomes de objetos. |
| [**IDMLOperator**](/windows/desktop/api/directml/nn-directml-idmloperator) | Representa um operador DirectML. |
| [**IDMLOperatorInitializer**](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer) | Representa um objeto especializado cuja finalidade é inicializar operadores compilados. |
| [**IDMLPageable**](/windows/desktop/api/directml/nn-directml-idmlpageable) | Implementado por objetos que podem ser removidos da memória GPU e, portanto, podem ser fornecidos para [IDMLDevice:: Remove](/windows/desktop/api/directml/nf-directml-idmldevice-evict) e [IDMLDevice:: MakeResident](/windows/desktop/api/directml/nf-directml-idmldevice-makeresident). |

## <a name="related-topics"></a>Tópicos relacionados

* [Referência do DirectML](direct3d-directml-reference.md)
* [Referência de núcleo](direct3d-12-core-reference.md)
* [Referência do Direct3D 12](direct3d-12-reference.md)
