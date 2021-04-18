---
description: Especifica um filtro de compactação a ser usado ao renderizar o grupo especificado.
ms.assetid: ba717cac-c5a8-4821-a5f0-dd9d5fe4834e
title: 'Método ISmartRenderEngine:: SetGroupCompressor (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.SetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9cb02a9d8daf7e6ba74a45299daa9d45ab63d5db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810214"
---
# <a name="ismartrenderenginesetgroupcompressor-method"></a>Método ISmartRenderEngine:: SetGroupCompressor

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

Especifica um filtro de compactação a ser usado ao renderizar o grupo especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetGroupCompressor(
   long        Group,
   IBaseFilter *pCompressor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Grupo* 
</dt> <dd>

Índice de base zero do grupo.

</dd> <dt>

*pCompressor* 
</dt> <dd>

Ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do filtro de compactação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface ISmartRenderEngine**](ismartrenderengine.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




