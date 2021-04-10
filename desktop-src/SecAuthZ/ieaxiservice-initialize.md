---
description: Verifica e baixa um objeto ActiveX.
ms.assetid: a477c6dc-32a7-4d17-a997-6df4967d6c55
title: 'Método IeAxiService:: Initialize'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Initialize
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2b2e388f955c968220223519150fc4dc5b7af4a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171678"
---
# <a name="ieaxiserviceinitialize-method"></a>Método IeAxiService:: Initialize

O método **Initialize** verifica e baixa um objeto ActiveX. Se o objeto atender aos requisitos da política, esse método inicializará um objeto do sistema que instala o objeto ActiveX.

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS Initialize(
  [in]  HWND     hwndParent,
  [in]  DWORD    dwClientPID,
  [in]  BSTR     bstrDesktop,
  [in]  BSTR     bstrClsID,
  [in]  BSTR     bstrURL,
  [out] BSTR     *pbstrNonce,
  [out] IUnknown **ppISyncBrokerInterface
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndParent* \[ no\]
</dt> <dd>

Um identificador para a janela pai da janela que está tentando instalar o controle ActiveX.

</dd> <dt>

*dwClientPID* \[ no\]
</dt> <dd>

A ID de processo do processo de chamada.

</dd> <dt>

*bstrDesktop* \[ no\]
</dt> <dd>

A área de trabalho para o objeto.

</dd> <dt>

*bstrClsID* \[ no\]
</dt> <dd>

A ID de classe do objeto ActiveX a ser instalado.

</dd> <dt>

*bstrURL* \[ no\]
</dt> <dd>

A URL do objeto ActiveX a ser instalado.

</dd> <dt>

*pbstrNonce* \[ fora\]
</dt> <dd>

Um contexto que pode ser usado para compartilhar informações de estado em chamadas para outros métodos usados para verificar e baixar o objeto ActiveX.

</dd> <dt>

*ppISyncBrokerInterface* \[ fora\]
</dt> <dd>

Um ponteiro para a instância da interface [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) que instala o controle ActiveX.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem sucedido, o valor de retorno será S \_ OK.

Se a função falhar, o valor de retorno poderá ser um dos códigos de erro a seguir.



| Código/valor de retorno                                                                                                                                                              | Descrição                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**Confiar \_ E \_ assunto \_ não \_ confiável**</dt> <dt>0x800B0004</dt> </dl> | O objeto ActiveX não deve ser instalado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Business, Windows Vista Enterprise, \[ somente aplicativos de área de trabalho do Windows Vista Ultimate\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiService é definido como E9E92380-9ECD-4982-A0EB-6815A56CCF27<br/>                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IeAxiService**](ieaxiservice.md)
</dt> </dl>

 

 




