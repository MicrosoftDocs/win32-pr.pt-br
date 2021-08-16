---
description: O método SetResizerGUID especifica o CLSID de um filtro de redimensionamento de vídeo personalizado.
ms.assetid: 709a6e7f-64ae-406d-bb6d-29f6c65b63a8
title: 'Método IRenderEngine2:: SetResizerGUID (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2.SetResizerGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e650a250333ac784e599d0bce820ef390a937f49bff2371b1b7a52b18d9d0ad6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818531"
---
# <a name="irenderengine2setresizerguid-method"></a>Método IRenderEngine2:: SetResizerGUID

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetResizerGUID` método especifica o CLSID de um filtro de redimensionamento de vídeo personalizado. chame esse método para substituir o filtro de redimensionamento padrão usado pelos serviços de edição DirectShow. O filtro deve ser registrado como um objeto COM no sistema do usuário e deve dar suporte à interface [**IResize**](iresize.md) .

Chame esse método antes de chamar [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetResizerGUID(
  [in] GUID ResizerGuid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ResizerGuid* \[ no\]
</dt> <dd>

O CLSID do filtro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Para reverter para o redimensionador DES padrão, use o seguinte CLSID:


```C++
// {F97B8A60-31AD-11CF-B2DE-00DD01101B85}
DEFINE_GUID(CLSID_Resize, 
0xF97B8A60, 0x31AD, 0x11CF, 0xB2, 0xDE, 0x00, 0xDD, 0x01, 0x10, 0x1B, 0x85);
```



> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> para obter o Qedit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | DirectX 9,0 ou posterior<br/>                                                         |
| Cabeçalho<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> <dt>

[**Interface IRenderEngine2**](irenderengine2.md)
</dt> </dl>

 

 




