---
description: O método SourceListAddSource adiciona uma fonte de rede ou URL. Aceita SourcePath, Type e Index como parâmetros. Esse método chama MsiSourceListAddSourceEx.
ms.assetid: 87797a8c-f1ba-4bfb-9296-3d3ef2a3c37f
title: Método Patch.SourceListAddSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListAddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 712551a31868ad3a97738ce9f49c9b0ff3526cf33cbae0ca5dd284f701869666
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519596"
---
# <a name="patchsourcelistaddsource-method"></a>Método Patch.SourceListAddSource

O **método SourceListAddSource** adiciona uma fonte de rede ou URL. Aceita *SourcePath*, *Tipo* e *Índice* como parâmetros. Esse método chama [**MsiSourceListAddSourceEx.**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)

## <a name="syntax"></a>Sintaxe


```JScript
Patch.SourceListAddSource(
  Type,
  SourcePath,
  Index
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Tipo* 
</dt> <dd>

Tipo de fonte a ser adicionada: MSISOURCETYPE \_ NETWORK ou URL MSISOURCETYPE. \_

</dd> <dt>

*Sourcepath* 
</dt> <dd>

Caminho para a origem a ser adicionada.

</dd> <dt>

*Index* 
</dt> <dd>

Se **SourceListAddSource** for chamado com uma nova fonte e *Index* definido como 0, o instalador adiciona a origem ao final da lista de origem.

Se essa função for chamada com uma origem  já existente na lista de origem e Index for definido como 0, o instalador manterá o índice existente da origem.

Se a função for chamada com uma fonte  existente na lista de origem e Index for definido como um valor diferente de zero, a origem será removida de seu local atual na lista e inserida na posição especificada por *Index*, antes de qualquer fonte que já exista nessa posição.

Se a função for chamada com uma nova origem e *Index* for definido como um valor não zero, a origem será inserida na posição especificada por *Index*, antes de qualquer fonte que já exista nessa posição. O valor do índice para todas as fontes na lista após o índice especificado por *Índice* é atualizado para garantir que os valores de índice exclusivos e a ordem preexistência permaneçam inalteradas.

Se *Index* for maior que o número de fontes na lista, a origem será colocada no final da lista com um valor de índice um maior que qualquer fonte existente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador 3.0 ou posterior no Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IPatch é definido como \_ 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
</dt> <dt>

[Sem suporte no Windows 2.0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




