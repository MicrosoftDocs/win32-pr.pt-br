---
title: Não há suporte para a chamada de ImmSetConversionStatus () ou ImmGetConversionStatus () de aplicativos da Windows Store
description: Não há suporte para a chamada de ImmSetConversionStatus () ou ImmGetConversionStatus () de aplicativos da Windows Store
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b0846b56b1d6c2367c46e4adf82dac011c49fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641198"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a>Não há suporte para a chamada de ImmSetConversionStatus () ou ImmGetConversionStatus () de aplicativos da Windows Store

## <a name="platforms"></a>Plataformas

<dl> Clientes-Windows 8,1  
Servidores-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Description

Não há suporte para a chamada de ImmSetConversionStatus () ou ImmGetConversionStatus () de um aplicativo da Windows Store e isso pode causar resultados inesperados.

## <a name="manifestations"></a>Manifestações

Na inicialização do aplicativo, o modo IME é definido com os seguintes padrões:



|          | Painel de entrada de software | Teclado de hardware |
|----------|----------------------|-------------------|
| KOR, JPN | Ativado                   | Desativado               |
| CHS, CHT | Ativado                   | Ativado                |



 

## <a name="solution"></a>Solução

Os desenvolvedores podem controlar o modo IME padrão especificando um valor de escopo de entrada para o campo.

O modo IME para um escopo de entrada especificado é determinado por cada IME. Os desenvolvedores não podem especificar o modo IME.

## <a name="resources"></a>Recursos

-   [Enumeração InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [ImmSetConversionStatus](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   [ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))

 

 