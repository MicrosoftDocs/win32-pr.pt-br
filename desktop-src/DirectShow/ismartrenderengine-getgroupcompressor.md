---
description: O método GetGroupCompressor recupera o filtro de compactação para o grupo especificado.
ms.assetid: 9d71e659-7abb-48c6-b9bd-5239560dc150
title: 'Método ISmartRenderEngine:: GetGroupCompressor (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.GetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 65915039d26b3c8739441240419e61e0cbacf5a6f4212cbb1c8b456f55dfcbd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817434"
---
# <a name="ismartrenderenginegetgroupcompressor-method"></a>Método ISmartRenderEngine:: GetGroupCompressor

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetGroupCompressor` método recupera o filtro de compactação para o grupo especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetGroupCompressor(
   long        Group,
   IBaseFilter **pCompressor
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

Recebe um ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do filtro de compactação. Ele receberá o valor **NULL** se não houver nenhum filtro de compactação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Use esse método para definir propriedades no filtro de compactação, como a taxa de quadros-chave. Chame esse método depois de chamar [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md), mas antes de renderizar o projeto. Em seguida, consulte o pino de saída do filtro de compactação para a interface [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) , que contém métodos para definir parâmetros de compactação. Libere a interface quando terminar. Se você fizer alterações subsequentes na linha do tempo, chame **ConnectFrontEnd** e chame **GetGroupCompressor** novamente para redefinir os parâmetros de compactação.

No retorno, se o valor de \* *pCompressor* for não **nulo**, a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

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

 

 




