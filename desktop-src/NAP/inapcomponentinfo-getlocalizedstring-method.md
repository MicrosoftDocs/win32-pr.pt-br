---
title: Método gettraduzistring INapComponentInfo (NapCommon. h)
description: É usado pelo sistema NAP para obter cadeias de caracteres localizadas.
ms.assetid: ad5be180-6329-4c91-b4d1-871a4d83c323
keywords:
- Método gettraduzistring NAP
- Método gettraduzistring NAP, interface INapComponentInfo
- INapComponentInfo interface NAP, método gettraduzistring
topic_type:
- apiref
api_name:
- INapComponentInfo.GetLocalizedString
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 781e4e8c93f58039c72a98f40a529243e5722d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919213"
---
# <a name="inapcomponentinfogetlocalizedstring-method"></a>Método INapComponentInfo:: gettraduzistring

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método de retorno de chamada **INapComponentInfo:: Gettraduzistring** é usado pelo sistema NAP para obter cadeias de caracteres localizadas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetLocalizedString(
  [in]  MessageId     msgId,
  [out] CountedString **string
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*msgid* \[ no\]
</dt> <dd>

Uma [**MessageId**](nap-datatypes.md) que contém a ID de recurso da cadeia de caracteres a ser localizado.

</dd> <dt>

*cadeia de caracteres* \[ fora\]
</dt> <dd>

Um ponteiro para um ponteiro para um [**contadostring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contém a versão localizada da mensagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorne um desses códigos de erro com base no resultado dessa operação.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | A operação teve êxito.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

As cadeias de caracteres devem ser localizadas de acordo com a ID do idioma do thread de chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





