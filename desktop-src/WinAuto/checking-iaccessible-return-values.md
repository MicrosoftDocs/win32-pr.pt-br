---
title: Verificando valores de retorno do IAccessible
description: Os desenvolvedores de cliente não devem confiar nas macros de Component Object Model (COM) com êxito e FALHAram em testar os valores de retorno de IAccessible, pois valores diferentes de S \_ OK são considerados um sucesso.
ms.assetid: 0def0349-178b-4be5-aa1d-6602dc015981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9328c89b0ab2b86e35cf06e74f05dd4937999be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105812059"
---
# <a name="checking-iaccessible-return-values"></a>Verificando valores de retorno do IAccessible

Os desenvolvedores de cliente não devem confiar nas macros de Component Object Model (COM) com [**êxito**](/windows/desktop/api/winerror/nf-winerror-succeeded) e [**falharam**](/windows/desktop/api/winerror/nf-winerror-failed) em testar os valores de retorno de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , pois valores diferentes de S \_ OK são considerados um sucesso. Por exemplo, um método pode retornar S \_ false, que é considerado um sucesso pela macro **Succeeded** , mas ainda recebe um ponteiro **NULL** em um parâmetro de saída.

Os desenvolvedores de cliente devem se proteger contra a possibilidade de que alguns servidores retornem códigos de erro diferentes dos valores documentados. Para ser seguro, você deve garantir que todos os parâmetros de saída contenham informações válidas e atendam aos seguintes critérios:

-   Todos os ponteiros são não **nulos**.
-   O membro **VT** de qualquer estrutura [Variant](/windows/win32/api/oaidl/ns-oaidl-variant) não é igual a VT \_ Empty.

 

 