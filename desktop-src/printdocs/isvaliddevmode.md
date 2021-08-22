---
description: A função IsValidDevmode verifica se o conteúdo de uma estrutura DEVMODE é válido.
ms.assetid: 8b4e32cc-5eeb-4a0d-a1b7-f6edb99ed8d8
title: Função IsValidDevmode (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsValidDevmode
- IsValidDevmodeA
- IsValidDevmodeW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 4c3a5cd33a6a5584ea9373df22df51a09e3e763d284a0f979f0b24e3651dc3d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100524"
---
# <a name="isvaliddevmode-function"></a>Função IsValidDevmode

A **função IsValidDevmode** verifica se o conteúdo de uma estrutura DEVMODE é válido.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsValidDevmode(
  _In_ PDEVMODE pDevmode,
       size_t   DevmodeSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevmode* \[ Em\]
</dt> <dd>

Um ponteiro para o [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) a ser validado.

</dd> <dt>

*DevmodeSize* 
</dt> <dd>

O tamanho em bytes do buffer de bytes de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**TRUE**, se [**o DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) for estruturalmente válido. Se ocorrerem erros secundários, a função os corrigirá e retornará **TRUE.**

**FALSE**, se o [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) tiver um ou mais problemas estruturais significativos. Por exemplo, seu **membro dmSize** é desalinhado ou especifica um buffer muito pequeno. Além disso, **FALSE** se **pDevmode** for **NULL.**

## <a name="remarks"></a>Comentários

Nenhum campo de driver de impressora privada [**do DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) é verificado, somente os campos públicos.

Os chamadores devem usar **dmSize** + **dmDriverExtra** para **DevmodeSize** somente se puderem garantir que o tamanho do buffer de entrada seja pelo menos tão grande. Como [**o DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) geralmente é dados não considerados, os valores que estão no buffer de entrada nos deslocamentos **dmSize** e **dmDriverExtra** também não são considerados.

Essa função é executável no Least-Privileged conta de usuário (LUA).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **IsValidDevmodeW** (Unicode) e **IsValidDevmodeA** (ANSI)<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> </dl>

 

 




