---
description: verifica e baixa um objeto de ActiveX.
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
ms.openlocfilehash: 911d955f84d81b225a1b4062e47b2b9b6ab6d058aa6df2e6a72a8d40242345a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414886"
---
# <a name="ieaxiserviceinitialize-method"></a>Método IeAxiService:: Initialize

o método **Initialize** verifica e baixa um objeto ActiveX. se o objeto atender aos requisitos da política, esse método inicializará um objeto do sistema que instala o objeto ActiveX.

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

um identificador para a janela pai da janela que está tentando instalar o controle de ActiveX.

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

a ID de classe do objeto de ActiveX a ser instalado.

</dd> <dt>

*bstrURL* \[ no\]
</dt> <dd>

a URL do objeto de ActiveX a ser instalado.

</dd> <dt>

*pbstrNonce* \[ fora\]
</dt> <dd>

um contexto que pode ser usado para compartilhar informações de estado em chamadas para outros métodos usados para verificar e baixar o objeto ActiveX.

</dd> <dt>

*ppISyncBrokerInterface* \[ fora\]
</dt> <dd>

um ponteiro para a instância da interface [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) que instala o controle de ActiveX.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem sucedido, o valor de retorno será S \_ OK.

Se a função falhar, o valor de retorno poderá ser um dos códigos de erro a seguir.



| Código/valor de retorno                                                                                                                                                              | Descrição                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**Confiar \_ E \_ assunto \_ não \_ confiável**</dt> <dt>0x800B0004</dt> </dl> | o objeto ActiveX não deve ser instalado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows vista Business, Windows vista Enterprise, \[ somente os aplicativos de área de trabalho do Windows vista Ultimate\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiService é definido como E9E92380-9ECD-4982-A0EB-6815A56CCF27<br/>                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IeAxiService**](ieaxiservice.md)
</dt> </dl>

 

 




