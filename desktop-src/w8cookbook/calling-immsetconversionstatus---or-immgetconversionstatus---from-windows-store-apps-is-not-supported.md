---
title: Não há suporte para chamar ImmSetConversionStatus() ou ImmGetConversionStatus() da Windows Store
description: Não há suporte para chamar ImmSetConversionStatus() ou ImmGetConversionStatus() da Windows Store
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9950bc008ce96d6c0a80a6090c3312057a12c4a7a1f64a5563625a518831c27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119348566"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a>Não há suporte para chamar ImmSetConversionStatus() ou ImmGetConversionStatus() da Windows Store

## <a name="platforms"></a>Plataformas

<dl> Clientes – windows 8.1  
Servidores – Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrição

Não há suporte para chamar ImmSetConversionStatus() ou ImmGetConversionStatus() de um aplicativo da Windows Store e pode causar resultados inesperados.

## <a name="manifestations"></a>Manifestações

Na configuração do aplicativo, o modo IME é definido com os seguintes padrões:



| &nbsp;   | Painel de entrada de software | Teclado de hardware |
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

 

 