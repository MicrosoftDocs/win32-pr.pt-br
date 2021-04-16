---
title: Método GetDescription do INapComponentInfo (NapCommon. h)
description: É usado pelo sistema NAP para obter a descrição de um cliente de integridade.
ms.assetid: f8d1d5ea-0de6-426d-90eb-b035b5bd0bfd
keywords:
- Método GetDescription NAP
- Método GetDescription NAP, interface INapComponentInfo
- INapComponentInfo interface NAP, método GetDescription
topic_type:
- apiref
api_name:
- INapComponentInfo.GetDescription
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 499aee6f7805925cc68c08b580db7b1b72763165
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105750462"
---
# <a name="inapcomponentinfogetdescription-method"></a>Método INapComponentInfo:: GetDescription

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método de retorno de chamada **INapComponentInfo:: GetDescription** é usado pelo sistema NAP para obter a descrição de um cliente de integridade.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDescription(
  [out] MessageId *description
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Descrição* \[ do fora\]
</dt> <dd>

Um ponteiro para uma [**MessageId**](nap-datatypes.md) que contém a ID de recurso da descrição.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorne um desses códigos de erro com base no resultado dessa operação.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | A operação teve êxito.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

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

 

 





