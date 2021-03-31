---
title: Método INapComponentConfig3 DeleteConfig (NapCommon. h)
description: É implementado por SHVs (validadores da integridade do sistema) para fornecer uma maneira de excluir dados de configuração para uma ID de configuração específica.
ms.assetid: 9740c122-86c8-4b77-9268-faa90e84d8aa
keywords:
- Método DeleteConfig NAP
- Método DeleteConfig NAP, interface INapComponentConfig3
- INapComponentConfig3 interface NAP, método DeleteConfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a9b9a6838616f0892b45df34d9a7c5ed63ff16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644511"
---
# <a name="inapcomponentconfig3deleteconfig-method"></a>INapComponentConfig3: método eleteConfig de:D

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **DeleteConfig** é implementado por SHVs (validadores da integridade do sistema) para fornecer uma maneira de excluir dados de configuração para uma ID de configuração específica. A ID pode ser reutilizada depois que os dados de configuração forem excluídos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeleteConfig(
   UINT32 configID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*configid* 
</dt> <dd>

Um valor que representa os dados de configuração a serem excluídos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos seguintes códigos de erro com base no resultado dessa operação.



| Código de retorno                                                                                                    | Description                                                                  |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | A operação teve êxito.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                   | *Configid* é 0 (um valor reservado para a configuração padrão).<br/> |
| <dl> <dt>**configuração de NAP \_ E \_ SHV \_ \_ não \_ encontrada**</dt> </dl> | Não foi possível encontrar *configid* .<br/>                                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





