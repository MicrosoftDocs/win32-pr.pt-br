---
title: Precauções de função de gancho de In-Context
description: Por motivos de desempenho, os desenvolvedores de cliente registram funções de gancho no contexto.
ms.assetid: 14b48920-a291-4519-b005-e559263a0e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c0e319037cb1295725548b3361bf076b4b1f760
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105771446"
---
# <a name="in-context-hook-function-precautions"></a>Precauções de função de gancho de In-Context

Por motivos de desempenho, os desenvolvedores de cliente registram funções de gancho no contexto. No entanto, como essas funções de conexão são mapeadas para o espaço de endereço do servidor, os desenvolvedores de cliente e servidor devem tomar precauções para garantir que o processamento do evento ocorra sem problemas.

## <a name="precautions-for-client-developers"></a>Precauções para desenvolvedores clientes

Os desenvolvedores de cliente devem estar cientes dos seguintes problemas:

-   Funções de gancho no contexto não devem usar muito tempo do processador, pois a função Hook deve retornar antes de o aplicativo do servidor continuar.
-   Depois que um evento é disparado, é possível que a janela associada a um evento não exista mais no momento em que a função de Hook é chamada. Os clientes devem verificar se a janela associada a um evento ainda existe antes de realizar qualquer outra ação relacionada ao evento. Para garantir que uma janela ainda exista, os clientes usam a função [**IsWindow**](/windows/desktop/api/winuser/nf-winuser-iswindow) do Microsoft Win32.
-   Se a DLL na qual a função de Hook é definida vincula-se a outra DLL, os desenvolvedores de cliente devem garantir que o sistema carregue a outra DLL. Se estiver vinculando implicitamente (usando arquivos. def e importações), a DLL adicional deverá estar no diretório do Windows ou em um dos diretórios do sistema, como o \\ sistema Windows, o Windows \\ System32 ou o Windows \\ SysWOW64. Se estiver vinculando explicitamente (usando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)), o caminho completo para o diretório no qual a dll adicional reside deve ser especificado na chamada para **LoadLibrary**.
-   As funções de gancho no contexto podem causar um estouro de pilha quando a DLL que contém a função de Hook é carregada em um aplicativo de 16 bits. Esse problema ocorre porque os aplicativos de 16 bits usam um tamanho de pilha fixo que não é grande o suficiente para acomodar a cadeia de chamadas de função do sistema que resultam em uma chamada para a função de gancho.

## <a name="precautions-for-server-developers"></a>Precauções para desenvolvedores de servidor

Os desenvolvedores de servidor precisam estar cientes de que os aplicativos cliente podem registrar funções de interceptação no contexto. Quando um servidor chama [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent), ele deve estar preparado para manipular o [**WM \_ GetObject**](wm-getobject.md) e outros métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

## <a name="invalid-interface-pointers"></a>Ponteiros de interface inválidos

Quando um cliente chama [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) dentro de uma função de gancho no contexto, o ponteiro da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que é retornado aponta diretamente para o código no espaço de endereço do servidor. Se o cliente chamar uma propriedade de interface usando esse ponteiro, a biblioteca de Component Object Model (COM) não estará envolvida com o marshaling (empacotamento e envio de parâmetros de interface entre limites de processo) ou desempacotamento (parâmetros de desempacotamento que foram enviados entre limites de processo) e não detectará se um objeto é destruído.

Se o cliente chamar uma propriedade de interface para um objeto que é destruído, o ponteiro de interface inválido causará uma falha de proteção geral no espaço de endereço do servidor, a menos que o servidor detecte essa situação.

Para proteger contra ponteiros de interface inválidos, os servidores [criam objetos de proxy](creating-proxy-objects.md) que encapsulam objetos acessíveis e monitoram a vida útil de objetos acessíveis. Por exemplo, quando um cliente chama uma propriedade [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para obter informações sobre um objeto, o proxy verifica se o objeto acessível ainda está disponível e, nesse caso, encaminha a solicitação do cliente para o objeto acessível. Se o objeto acessível for destruído, o proxy retornará um erro ao cliente.

 

 