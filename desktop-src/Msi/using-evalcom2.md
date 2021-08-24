---
description: Evalcom2.dll pode ser usado para implementar operações de validação para pacotes de instalação e módulos de mesclagem usando Avaliadores de Consistência Interna – ICEs.
ms.assetid: df38e75e-554c-4a6d-b9ad-8eee5123a16f
title: Usando Evalcom2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f89ba0215e697cb03111daa80510e6ba6c677c2e74f31e74b5640340d2d0d9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527117"
---
# <a name="using-evalcom2"></a>Usando Evalcom2

Evalcom2.dll pode ser usado para implementar operações de validação para pacotes de instalação e módulos de mesclagem usando Avaliadores de Consistência Interna [– ICEs](internal-consistency-evaluators-ices.md). O objeto principal implementa interfaces para programas C/C++.

O objeto principal também implementa interfaces [Evalcom2](evalcom2-interfaces.md) para programas C/C++. O CLSID necessário para obter a interface de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) é {6E5E1910-8053-4660-B795-6B612E29BC58}. A REFIID é {E482E5C6-E31E-4143-A2E6-DBC3D8E4B8D3}.

Você pode usar o procedimento a seguir para implementar operações de validação.

**Para implementar operações de validação**

1.  Inicialize COM no thread de chamada usando [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).
2.  Obtenha o ponteiro para a interface [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) usando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).
3.  Abra o pacote de instalação ou o módulo de mesclagem usando o [**método OpenDatabase.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opendatabase)
4.  Abra o arquivo de avaliação usando o [**método OpenCUB.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub)
5.  De definir a função de retorno de chamada de exibição usando [**o método SetDisplay.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay)
6.  De definir a função de retorno de chamada de status usando [**o método SetStatus.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus)
7.  Execute a validação usando o [**método Validate.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-validate)
8.  Feche o arquivo .file usando o [**método CloseCUB.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closecub)
9.  Feche o banco de dados usando [**o método CloseDatabase.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closedatabase)
10. Libere a interface [**IValidate.**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate)
11. Não reinicializar COM usando [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Evalcom2 Interfaces](evalcom2-interfaces.md)
</dt> <dt>

[Automação de Validação](validation-automation.md)
</dt> <dt>

[Funções de retorno de chamada de validação](validation-callback-functions.md)
</dt> </dl>

 

 
