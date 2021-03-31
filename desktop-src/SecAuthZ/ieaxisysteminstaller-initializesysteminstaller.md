---
description: Instala o objeto ActiveX especificado.
ms.assetid: c5d460d8-0df4-437a-a59e-707bf868a339
title: 'Método IeAxiSystemInstaller:: InitializeSystemInstaller'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller.InitializeSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: 874bee80e23051d5dfdd22e259395293ae532619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829736"
---
# <a name="ieaxisysteminstallerinitializesysteminstaller-method"></a>Método IeAxiSystemInstaller:: InitializeSystemInstaller

O método **InitializeSystemInstaller** instala o objeto ActiveX especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT InitializeSystemInstaller(
  [in]  BSTR     bstrUrl,
  [in]  DWORD    dwClientPID,
  [in]  IUnknown *pCallback,
  [out] BSTR     *pbstrNonce
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrUrl* \[ no\]
</dt> <dd>

A URL do objeto ActiveX a ser instalado.

</dd> <dt>

*dwClientPID* \[ no\]
</dt> <dd>

A ID de processo do processo de chamada.

</dd> <dt>

*pCallback* \[ no\]
</dt> <dd>

Um ponteiro para uma instância da interface [**IeAxiServiceCallback**](ieaxiservicecallback.md) que verifica se o objeto ActiveX tem permissão para ser instalado.

</dd> <dt>

*pbstrNonce* \[ fora\]
</dt> <dd>

Um contexto que pode ser usado para compartilhar informações de estado em chamadas para outros métodos usados para verificar e baixar o objeto ActiveX.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem sucedido, o método retornará S \_ OK.

Se o método falhar, ele retornará um valor **HRESULT** que indica o erro. Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Business, Windows Vista Enterprise, \[ somente aplicativos de área de trabalho do Windows Vista Ultimate\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiSystemInstaller é definido como a50ea6f8-4764-4299-b309-022b2a8b4d8d<br/>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IeAxiSystemInstaller**](ieaxisysteminstaller.md)
</dt> </dl>

 

