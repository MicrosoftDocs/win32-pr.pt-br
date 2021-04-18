---
description: A função IsValidDevmode verifica se o conteúdo de uma estrutura DEVMODE é válido.
ms.assetid: 8b4e32cc-5eeb-4a0d-a1b7-f6edb99ed8d8
title: Função IsValidDevmode (winspool. h)
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
ms.openlocfilehash: 0b8a940fd08e1ab19b18969a763448b65fffd9d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105816034"
---
# <a name="isvaliddevmode-function"></a>Função IsValidDevmode

A função **IsValidDevmode** verifica se o conteúdo de uma estrutura DEVMODE é válido.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsValidDevmode(
  _In_ PDEVMODE pDevmode,
       size_t   DevmodeSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevmode* \[ no\]
</dt> <dd>

Um ponteiro para o [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) a ser validado.

</dd> <dt>

*DevmodeSize* 
</dt> <dd>

O tamanho em bytes do buffer de bytes de entrada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

**True**, se o [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) for estruturalmente válido. Se forem encontrados erros secundários, a função os corrigirá e retornará **true**.

**False**, se o [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) tiver um ou mais problemas estruturais significativos. Por exemplo, seu membro **dmSize** está desalinhado ou especifica um buffer muito pequeno. Além disso, **false** se **pDevmode** for **nulo**.

## <a name="remarks"></a>Comentários

Nenhum campo de driver de impressora privada do [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) está marcado, somente os campos públicos.

Os chamadores devem usar **dmSize** + **dmDriverExtra** para **DevmodeSize** somente se puderem garantir que o tamanho do buffer de entrada seja pelo menos tão grande. Como o [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) geralmente é um dado não confiável, os valores que estão no buffer de entrada nos deslocamentos **dmSize** e **dmDriverExtra** também são não confiáveis.

Essa função é executável no contexto de LUA (Least-Privileged User Account).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Winspool. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **IsValidDevmodeW** (Unicode) e **IsValidDevmodeA** (ANSI)<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> </dl>

 

 




