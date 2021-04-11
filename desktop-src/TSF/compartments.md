---
title: Compartimentos
description: Compartimentos
ms.assetid: 7bffab6f-be40-4d3a-9342-6f81557a9656
keywords:
- TSF (estrutura de serviços de texto), compartimentos
- TSF (estrutura de serviços de texto), compartimentos
- serviços de texto, compartimentos
- Aplicativos habilitados para TSF, compartimentos
- compartimentos
- TSF (estrutura de serviços de texto), tipos de compartimentos
- TSF (estrutura de serviços de texto), tipos de compartimentos
- serviços de texto, tipos de compartimentos
- Aplicativos habilitados para TSF, tipos de compartimentos
- tipos de compartimentos
- TSF (estrutura de serviços de texto), notificações de alteração de compartimento
- TSF (estrutura de serviços de texto), notificações de alteração de compartimento
- serviços de texto, notificações de alteração de compartimento
- Aplicativos habilitados para TSF, notificações de alteração de compartimento
- notificações de alteração de compartimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76636c684ee74f7e452b5602ebfd59d6d1947b0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159568"
---
# <a name="compartments"></a>Compartimentos

## <a name="compartment-types"></a>Tipos de compartimentos

Há vários tipos diferentes de compartimentos. Há um compartimento global, e cada Gerenciador de threads, o Gerenciador de documentos e o contexto podem conter um compartimento.

O compartimento global permite que os clientes compartilhem dados entre processos. Para obter o Gerenciador de compartimento global, chame [**ITfThreadMgr:: GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment).

O Gerenciador de threads contém um Gerenciador de compartimentos que contém as compartimentos por thread. Isso permite que os dados sejam compartilhados em um thread. Para obter um Gerenciador de compartimentos do Gerenciador de threads, chame **ITfThreadMgr:: QueryInterface** com \_ ITfCompartmentMgr IID.

Cada Gerenciador de documentos criado também contém um Gerenciador de compartimentos. Isso permite que os dados sejam compartilhados em um gerente de documento específico. Para obter o Gerenciador de compartimento do Gerenciador de documentos, chame **ITfDocumentMgr:: QueryInterface** com \_ ITfCompartmentMgr IID.

Cada contexto criado também contém um Gerenciador de compartimentos. Isso permite que os dados sejam compartilhados em um contexto específico. Para obter um Gerenciador de compartimento de contexto, chame **ITfContext:: QueryInterface** com \_ ITfCompartmentMgr IID.

## <a name="creating-and-deleting-a-compartment"></a>Criando e excluindo um compartimento

Um compartimento é criado na primeira vez que [**ITfCompartmentMgr:: getcompartmentid**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment) é chamado com o GUID do compartimento. O cliente de instalação deve definir o valor inicial do compartimento usando [**ITfCompartment:: SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue). Até que um valor seja definido, o valor do compartimento estará vazio. Por isso, não é possível verificar se o compartimento existia antes que **getcompartmentid** fosse chamado. Para evitar essa situação, o cliente de instalação deve definir o valor como um valor inicial para que outros clientes possam determinar se o compartimento já existe.

O método [**ITfCompartmentMgr:: ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment) é usado para remover um compartimento. Todas as referências existentes ao compartimento são marcadas como inválidas.

## <a name="obtaining-compartments"></a>Obtendo compartimentos

Usando a interface [**ITfCompartmentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr) , um cliente pode enumerar compartimentos chamando [**ITfCompartmentMgr:: EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments). Esse método fornece um objeto **IEnumGUID** que contém os GUIDs de todos os compartimentos instalados.

Usando o GUID do compartimento, **ITfCompartmentMgr:: getcompartmentid** é usado para obter um compartimento específico. Esse método fornece ao chamador um objeto [**ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment) que pode obter e definir os dados do compartimento.

## <a name="receiving-compartment-change-notifications"></a>Recebendo notificações de alteração de compartimento

Quando o valor de um compartimento é alterado, o Gerenciador de TSF notifica todos os coletores de aviso instalados de que o compartimento foi alterado. Para instalar um coletor de aviso de alteração de compartimento, crie um objeto que implemente [**ITfCompartmentEventSink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink). Em seguida, chame **ITfCompartment:: QueryInterface** com ITFSOURCE de IID \_ no objeto de compartimento a ser monitorado para obter uma interface [**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource) . Agora, chame [**ITfSource:: AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) com IID \_ ITfCompartmentEventSink e o ponteiro para o objeto **ITfCompartmentEventSink** . Quando o valor do compartimento é alterado, o [**ITfCompartmentEventSink:: OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange) do coletor de aviso é chamado com o GUID do compartimento. O coletor de aviso pode chamar [**ITfCompartment:: GetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-getvalue) para obter o novo valor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ITfCompartmentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr)
</dt> <dt>

[**ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment)
</dt> <dt>

[**ITfCompartmentEventSink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink)
</dt> <dt>

[**TfClientId**](tfclientid.md)
</dt> <dt>

[**ITfThreadMgr::GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment)
</dt> <dt>

[**ITfCompartmentMgr:: getcompartmentid**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment)
</dt> <dt>

[**ITfCompartment:: SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue)
</dt> <dt>

[**ITfCompartmentMgr::ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment)
</dt> <dt>

[**ITfCompartmentMgr::EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments)
</dt> <dt>

[**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource)
</dt> <dt>

[**ITfSource:: AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> <dt>

[**ITfCompartmentEventSink:: OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange)
</dt> </dl>

 

 




