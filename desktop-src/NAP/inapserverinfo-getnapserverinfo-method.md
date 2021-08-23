---
title: Método GetNapServerInfo INapServerInfo (NapServerManagement.h)
description: Recupera informações sobre o servidor NAP.
ms.assetid: 02f7ce40-3443-4263-86b2-4276cbc7b694
keywords:
- NAP do método GetNapServerInfo
- Método GetNapServerInfo NAP, interface INapServerInfo
- NAP da interface INapServerInfo, método GetNapServerInfo
topic_type:
- apiref
api_name:
- INapServerInfo.GetNapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eec9926e1a0bf94a1e3dac38c01a169d596c1c00bf032b8f6954f6331d5a4d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626126"
---
# <a name="inapserverinfogetnapserverinfo-method"></a>Método INapServerInfo::GetNapServerInfo

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método INapServerInfo::GetNapServerInfo** recupera informações sobre o servidor NAP.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetNapServerInfo(
  [out] CountedString **serverName,
  [out] CountedString **serverDescription,
  [out] CountedString **protocolVersion
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*serverName* \[ out\]
</dt> <dd>

Um ponteiro para um ponteiro para uma [**estrutura CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contém o nome do servidor.

</dd> <dt>

*serverDescription* \[ out\]
</dt> <dd>

Um ponteiro para um ponteiro para uma estrutura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contém a descrição do servidor.

</dd> <dt>

*protocolVersion* \[ out\]
</dt> <dd>

Um ponteiro para um ponteiro para uma estrutura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contém a versão do protocolo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos do COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Êxito na operação.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite de recursos do sistema, não foi possível executar a operação.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                               |
| Cabeçalho<br/>                   | <dl> <dt>NapServerManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapServerManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapServerInfo**](inapserverinfo.md)
</dt> <dt>

[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)
</dt> </dl>

 

 





