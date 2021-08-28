---
description: O método SetDynamicReconnectLevel define o nível de reconexão dinâmica durante a renderização.
ms.assetid: 092f3464-84a2-48b0-9647-66fe27e9706d
title: 'Método IRenderEngine:: SetDynamicReconnectLevel (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetDynamicReconnectLevel
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b43967753dd03d213a322ce569d113346542a57b5f37fd69fc28937198109049
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083676"
---
# <a name="irenderenginesetdynamicreconnectlevel-method"></a>Método IRenderEngine:: SetDynamicReconnectLevel

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetDynamicReconnectLevel` método define o nível de reconexão dinâmica durante a renderização.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetDynamicReconnectLevel(
   DWORD Level
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Level* 
</dt> <dd>

Combinação de [**sinalizadores de reconexão dinâmica**](dynamic-reconnection-flags.md), especificando o nível de reconexão dinâmica.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes valores de **HRESULT** :



| Código de retorno                                                                               | Descrição                 |
|-------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Êxito.<br/>         |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Não implementado.<br/> |



 

## <a name="remarks"></a>Comentários

Por padrão, o mecanismo de processamento básico carrega cada fonte antes de renderizar um projeto. Isso pode resultar em um longo tempo de inicialização. Com a reconexão dinâmica, as fontes são carregadas somente quando necessário. Isso pode reduzir o tempo de inicialização, mas possivelmente interferir na reprodução suave. Em geral, quanto mais clipes de origem forem usados por um projeto, mais você poderá se beneficiar da reconexão dinâmica.

O mecanismo de processamento inteligente não implementa esse método.

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

[**Interface IRenderEngine**](irenderengine.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




