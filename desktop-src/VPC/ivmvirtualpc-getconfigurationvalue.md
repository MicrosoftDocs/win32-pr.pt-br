---
title: Método IVMVirtualPC GetConfigurationValue (VPCCOMInterfaces.h)
description: Recupera o valor da definição de configuração especificada.
ms.assetid: 4598b57c-9942-4b40-97b5-41ad9ec74bfa
keywords:
- Pc Virtual do método GetConfigurationValue
- Método GetConfigurationValue PC virtual, interface IVMVirtualPC
- Interface IVMVirtualPC pc virtual , método GetConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a483211353474f3328fc4e5da3b80ecf3fbbece53bc306e546f85543ac9027e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591857"
---
# <a name="ivmvirtualpcgetconfigurationvalue-method"></a>Método IVMVirtualPC::GetConfigurationValue

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o valor da definição de configuração especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    preferenceKey,
  [out, retval] VARIANT *preferenceValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*preferenceKey* \[ Em\]
</dt> <dd>

A chave usada para identificar a preferência, conforme armazenado no arquivo de configuração.

</dd> <dt>

*preferenceValue* \[ out, retval\]
</dt> <dd>

O valor de preferência. Esse parâmetro pode ser um dos seguintes tipos **VARIANT:** **VT \_ ARRAY** \| **VT \_ UI1** (bytes brutos), **VT \_ BSTR** (cadeia de caracteres), **VT \_ I4** (inteiro) ou **BOOL VT \_ (booliana).**

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                                        | Descrição                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | A operação foi bem-sucedida.<br/>                                                        |
| <dl> <dt>**E \_ PONTEIRO**</dt> <dt>0x80004003</dt> </dl>                                | O *parâmetro preferenceKey* ou *preferenceValue* é **NULL.**<br/>                      |
| <dl> <dt>**VM \_ E \_ PREF \_ NÃO ENCONTRADO \_ 0XA0040300**</dt> <dt></dt> </dl>                   | A preferência não foi encontrada.<br/>                                                        |
| <dl> <dt>**VM \_ VIRTUALIZAÇÃO \_ DE HARDWARE E \_ \_ DESABILITADA**</dt> <dt>0XA0040951</dt> </dl> | O processador não dá suporte a extensões de HAV (Virtualização Acelerada de Hardware).<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Ocorreu um erro inesperado.<br/>                                                    |



 

## <a name="remarks"></a>Comentários

Esse método fornece acesso de baixo nível a qualquer valor de preferência para o usuário atual. Ele pode ser usado para recuperar valores de preferência para chaves definidas pelo cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC é definido como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

