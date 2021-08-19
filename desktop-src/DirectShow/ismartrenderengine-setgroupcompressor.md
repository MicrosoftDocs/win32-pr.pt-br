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
ms.openlocfilehash: 002c1e9e6bbb2ea223fb208586b250455e2a1a6273babe2f8e38a51271ab8426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817157"
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

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> para obter o Qedit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

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

 

 




