---
title: Método IVMVirtualPC RemoveConfigurationValue (VPCCOMInterfaces.h)
description: Remove o valor da configuração especificada.
ms.assetid: 07bafa5e-bf62-45bf-af4e-a66050f5afad
keywords:
- Pc Virtual do método RemoveConfigurationValue
- Método RemoveConfigurationValue pc virtual , interface IVMVirtualPC
- Interface IVMVirtualPC pc virtual , método RemoveConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualPC.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 281837394967a15bce40173ead0ca02be66eb046bf7c15b63fdded57c2ecef84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998527"
---
# <a name="ivmvirtualpcremoveconfigurationvalue-method"></a>Método IVMVirtualPC::RemoveConfigurationValue

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Remove o valor da configuração especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR preferenceKey
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*preferenceKey* \[ Em\]
</dt> <dd>

A chave usada para identificar a preferência, conforme armazenado no arquivo de configuração.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                                        | Descrição                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | A operação foi bem-sucedida.<br/>                                                        |
| <dl> <dt>**E \_ PONTEIRO**</dt> <dt>0x80004003</dt> </dl>                                | O *parâmetro preferenceKey* é **NULL.**<br/>                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                             | O *parâmetro preferenceKey* não é válido ou é uma cadeia de caracteres vazia.<br/>                    |
| <dl> <dt>**VM \_ E \_ PREF \_ NÃO ENCONTRADO \_ 0XA0040300**</dt> <dt></dt> </dl>                   | A preferência não foi encontrada.<br/>                                                        |
| <dl> <dt>**VM \_ VIRTUALIZAÇÃO \_ DE HARDWARE E \_ \_ DESABILITADA**</dt> <dt>0XA0040951</dt> </dl> | O processador não dá suporte a extensões de HAV (Virtualização Acelerada de Hardware).<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Ocorreu um erro inesperado.<br/>                                                    |



 

## <a name="remarks"></a>Comentários

Esse método fornece acesso de baixo nível a qualquer valor de preferência para o usuário atual. Ele pode ser usado para remover valores de preferência para chaves definidas pelo cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC é definido como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

