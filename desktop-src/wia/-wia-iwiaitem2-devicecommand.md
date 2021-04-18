---
description: Emite um comando para um dispositivo de hardware de aquisição de imagem do Windows (WIA) 2,0.
ms.assetid: a077448f-2029-4fd3-8bce-c0291afd0b79
title: 'IWiaItem2: método eviceCommand de:D (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceCommand
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2961a3c0e0d1b75a487b9bf112e76bee8c937a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788661"
---
# <a name="iwiaitem2devicecommand-method"></a>IWiaItem2: método eviceCommand de:D

Emite um comando para um dispositivo de hardware de aquisição de imagem do Windows (WIA) 2,0.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeviceCommand(
  [in]            LONG      lFlags,
  [in]      const GUID      *pCmdGUID,
  [in, out]       IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Atualmente não utilizado. Deve ser definido como zero.

</dd> <dt>

*pCmdGUID* \[ no\]
</dt> <dd>

Tipo: **const GUID \** _

Especifica o comando a ser enviado para o dispositivo WIA 2,0. Consulte [_ *comandos* * do dispositivo WIA](-wia-wia-device-commands.md).

</dd> <dt>

*ppIWiaItem2* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Recebe o endereço de um ponteiro para o item [**IWiaItem2**](-wia-iwiaitem2.md) criado pelo comando, se houver.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Além dos códigos de erro COM padrão, o método pode retornar o valor a seguir.



| Código de retorno                                                                                       | Descrição                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ CMDNOTSUPPORTED**</dt> </dl> | O comando não é implementado para a interface [**IWiaItem2**](-wia-iwiaitem2.md) na qual o método é chamado. O valor numérico para esse erro ainda não foi definido. <br/> |



 

## <a name="remarks"></a>Comentários

O comportamento desse método é diferente dependendo da categoria do nó no qual o método é chamado.

Quando o aplicativo envia o comando do [**WIA \_ cmd \_ Take \_ Picture**](-wia-wia-device-commands.md) para o dispositivo usando o método **IWiaItem2::D evicecommand** , o sistema de tempo de execução WIA 2,0 cria um objeto [**IWiaItem2**](-wia-iwiaitem2.md) para representar a imagem. O método **IWiaItem2::D evicecommand** armazena o endereço da interface no parâmetro *ppIWiaItem2* .

Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppIWiaItem2* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
