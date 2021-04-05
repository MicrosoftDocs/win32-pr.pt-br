---
title: Método GetIcon INapComponentInfo (NapCommon. h)
description: É usado pelo sistema NAP para obter o ícone de um cliente de integridade.
ms.assetid: 6501fe12-1ec0-43a1-b672-b6cfd9a08d85
keywords:
- Método GetIcon NAP
- Método GetIcon NAP, interface INapComponentInfo
- INapComponentInfo interface NAP, método GetIcon
topic_type:
- apiref
api_name:
- INapComponentInfo.GetIcon
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 795ad85f8497262f88fa55d8efb2da7466b8c3a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919064"
---
# <a name="inapcomponentinfogeticon-method"></a>Método INapComponentInfo:: GetIcon

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método de retorno de chamada **INapComponentInfo:: GetIcon** é usado pelo sistema NAP para obter o ícone de um cliente de integridade.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetIcon(
  [out] CountedString **dllFilePath,
  [out] UINT32        *iconResourceId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dllFilePath* \[ fora\]
</dt> <dd>

Um ponteiro para um ponteiro para um [**contadostring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) usado para retornar o caminho do arquivo da dll que contém o ícone.

</dd> <dt>

*iconResourceId* \[ fora\]
</dt> <dd>

Um ponteiro para o valor usado para retornar a ID de recurso do ícone a ser usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorne um desses códigos de erro com base no resultado dessa operação.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | A operação teve êxito.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

Os ícones devem ser localizados de acordo com a ID do idioma do thread de chamada.

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

 

 





