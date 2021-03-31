---
title: O manipulador de Client-Side leve
description: Os manipuladores leves do lado do cliente permitem criar manipuladores gerais do lado do cliente de qualquer tamanho, para ajudá-lo a fazer qualquer tipo de tarefa padrão.
ms.assetid: b712237c-55d7-4f52-9cf6-19c6e5fb3182
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1e8df5be24e8773a660a4d0208b27a2f585e32
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641909"
---
# <a name="the-lightweight-client-side-handler"></a>O manipulador de Client-Side leve

Os manipuladores leves do lado do cliente permitem criar manipuladores gerais do lado do cliente de qualquer tamanho, para ajudá-lo a fazer qualquer tipo de tarefa padrão. Como manipuladores, eles podem ser usados por mais de um cliente. Elas diferem dos manipuladores OLE, pois não podem ser criadas antes de o servidor ser iniciado, e seu tempo de vida está vinculado ao Gerenciador de proxy, impedindo uma possível condição de corrida na qual o manipulador poderia, de outra forma, ser lançado prematuramente.

O Gerenciador de proxy é o objeto criado pelo sistema que implementa a interface [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) . Se você usar o marshaling padrão, o sistema o criará para você quando chamar [**CoGetStandardMarshal**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstandardmarshal) (ou [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex), para criar um marshaler agregado para manipuladores leves) e também implementará as interfaces [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) e [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi) no objeto. No lado do servidor, há um objeto do sistema correspondente que também implementa **IMarshal**. Esses objetos manipulam o marshaling para você de forma transparente.

Há dois tipos gerais desses manipuladores que você talvez queira implementar:

-   Um manipulador que executa um serviço que não requer dados adicionais do servidor
-   Um manipulador que usa dados adicionais do servidor

Alguns usos potenciais dos dados adicionais no fluxo fornecido pelo servidor são os seguintes:

-   Dados estáticos do servidor. Independentemente da interface específica que está sendo empacotada, o servidor grava os mesmos dados no fluxo.
-   Dados por interface do servidor. Dependendo de qual interface específica está sendo empacotada, o servidor pode gravar dados diferentes no fluxo.
-   Auxiliares por interface. Componentes COM por interface agregados ao manipulador de cliente e à delegação ao proxy padrão. Por exemplo, para melhorar o desempenho da rede, um componente COM para [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) poderia fazer cache de dados do lado do cliente, leitura antecipada, gravação por trás, bloqueio de op e assim por diante.
-   Versão de rede de uma interface. A versão de rede da interface é diferente da interface exposta pelo código do aplicativo cliente e servidor. É possível, por exemplo, multiplexar interfaces expostas IA e IB sobre o mesmo adaptador de rede INetAB, a maneira que o manipulador de servidor de incorporação faz. Por exemplo, é possível converter uma interface de transferência de dados em uma interface de rede que usa pipes para transferência de dados eficiente.

Os clientes de nível inferior podem não ter a capacidade de desempacotamento de interfaces que têm manipuladores personalizados, por dois motivos: primeiro, eles podem não entender o CLSID usado no pacote empacotado personalizado quando o manipulador de servidor é agregado e o objeto deseja um manipulador. Em segundo lugar, o código do manipulador pode nem mesmo ser executado no lado do cliente se ele exigir uma nova funcionalidade de COM para criar o marshaler padrão agregado e fazer chamadas de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) remotas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O manipulador OLE](the-ole-handler.md)
</dt> </dl>

 

 