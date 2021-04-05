---
title: Método de inicialização de INapSoHProcessor (NapProtocol. h)
description: Inicializa o pacote de protocolo e o sistema de processador SoH. Esse método deve ser chamado exatamente uma vez.
ms.assetid: 4fccc847-3c4d-4fc5-935d-28fb2964a9be
keywords:
- Inicializar método NAP
- Método Initialize NAP, interface INapSoHProcessor
- INapSoHProcessor interface NAP, método Initialize
topic_type:
- apiref
api_name:
- INapSoHProcessor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ff3a32bb213caf19964ccea8175a43e5016f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918449"
---
# <a name="inapsohprocessorinitialize-method"></a>Método INapSoHProcessor:: Initialize

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSoHProcessor:: Initialize** Inicializa o pacote de protocolo e o sistema de processador soh. Esse método deve ser chamado exatamente uma vez.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Initialize(
  [in]  const SoH                  *soh,
  [in]        BOOL                 isRequest,
  [out]       SystemHealthEntityId *id
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*soh* \[ no\]
</dt> <dd>

Um ponteiro para o pacote [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) a ser processado.

</dd> <dt>

*Isrequest* \[ no\]
</dt> <dd>

Um **bool** que será **verdadeiro** se o pacote for um [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) e **false** se for um **SoHResponse**.

</dd> <dt>

saída da *ID* \[\]
</dt> <dd>

Um [SystemHealthEntityId](nap-datatypes.md) exclusivo que contém a ID do SHA ou SHV que construiu o pacote.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                            | Descrição                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operação bem-sucedida.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | O limite de recursos do sistema não pôde executar a operação.<br/> |
| <dl> <dt>**\_pacote NAP E \_ inválido \_**</dt> </dl> | O pacote SoH é inválido.<br/>                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





