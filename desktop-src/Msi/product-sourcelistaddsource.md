---
description: O método SourceListAddSource adiciona uma fonte de rede ou URL. Aceita SourcePath, tipo e índice como parâmetros. Esse método chama MsiSourceListAddSourceEx.
ms.assetid: 61a8873f-c4ad-43d7-8bbb-5a2534ef2de7
title: Método Product. SourceListAddSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListAddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b95185cbd25354314eace5da7704da51dbbefe024ba8597c0eed41a688984117
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925858"
---
# <a name="productsourcelistaddsource-method"></a>Método Product. SourceListAddSource

O método **SourceListAddSource** adiciona uma fonte de rede ou URL. Aceita *SourcePath*,*tipo* e *índice* como parâmetros. Esse método chama [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa).

## <a name="syntax"></a>Sintaxe


```JScript
Product.SourceListAddSource(
  Type,
  SourcePath,
  Index
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Tipo* 
</dt> <dd>

Tipo de fonte a ser adicionada: MSISOURCETYPE \_ rede ou URL de MSISOURCETYPE \_ .

</dd> <dt>

*SourcePath* 
</dt> <dd>

Caminho para a origem a ser adicionada.

</dd> <dt>

*Index* 
</dt> <dd>

Se **SourceListAddSource** for chamado com uma nova origem e um *índice* for definido como 0, o instalador adicionará a origem ao final da lista de origem.

Se essa função for chamada com uma fonte já existente na lista de origem e o *índice* estiver definido como 0, o instalador manterá o índice existente da origem.

Se a função for chamada com uma origem existente na lista de origem e o *índice* for definido como um valor diferente de zero, a origem será removida de seu local atual na lista e inserida na posição especificada pelo *índice*, antes de qualquer fonte que já exista nessa posição.

Se a função for chamada com uma nova origem e um *índice* for definido como um valor diferente de zero, a origem será inserida na posição especificada pelo *índice*, antes de qualquer fonte que já exista nessa posição. O valor de índice para todas as fontes na lista após o índice especificado pelo *índice* é atualizado para garantir que os valores de índice exclusivos e a ordem pré-existente permaneçam inalterados.

Se o *índice* for maior que o número de fontes na lista, a origem será colocada no final da lista com um valor de índice maior do que qualquer origem existente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct é definido como 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Remessa**](product-object.md)
</dt> <dt>

[**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
</dt> <dt>

[sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




