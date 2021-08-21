---
title: Método getactivationvalue IVMVirtualMachine (VPCCOMInterfaces. h)
description: Recupera o valor da configuração de ativação especificada para esta máquina virtual.
ms.assetid: 9a6f138f-6a8a-4cdf-8fb3-83d541d88fba
keywords:
- PC virtual do método getactivationvalue
- Método getactivavalue Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, getactivationvalue método
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GetActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1e03d1178df5961ba76a0ab61e74c781315cce07f32657903e5fa3e4e0a7623
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123187"
---
# <a name="ivmvirtualmachinegetactivationvalue-method"></a>Método IVMVirtualMachine:: getactivationvalue

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o valor da configuração de ativação especificada para esta máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetActivationValue(
  [in]          BSTR    activationKey,
  [out, retval] VARIANT *activationValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*activationKey* \[ no\]
</dt> <dd>

A chave usada para identificar o valor de ativação, como armazenado no \* arquivo ". vmc".

</dd> <dt>

*activationvalue* \[ out, retval\]
</dt> <dd>

O valor de ativação. Esse valor pode ser um dos seguintes tipos **variantes** : **VT \_ array** \| **VT \_ UI1** (bytes brutos), **VT \_ BSTR** (String), **VT \_ i4** (Integer) ou **VT \_ bool** (booliano).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                      | Descrição                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                            | A operação foi bem-sucedida.<br/>                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>           | O parâmetro *activationKey* é **nulo** ou está vazio.<br/>                          |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>              | O parâmetro *activationvalue* é **nulo**.<br/>                                 |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>      | A configuração é desconhecida.<br/>                                                |
| <dl> <dt>**VM \_ E \_ pref \_ não \_ encontrado**</dt> <dt>0xA0040300</dt> </dl> | A preferência não foi encontrada ou essa configuração não tem ativação válida.<br/> |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>      | Ocorreu um erro inesperado.<br/>                                            |



 

## <a name="remarks"></a>Comentários

Esse método fornece acesso de baixo nível a qualquer valor de ativação. Ele pode ser usado para definir valores de ativação para chaves definidas pelo cliente. Quando uma máquina virtual é iniciada, uma cópia é feita de seus valores de configuração, que se torna seu conjunto de valores de ativação. Os valores de ativação são mantidos até que a máquina virtual seja desligada ou reiniciada. observe que Windows Virtual PC só pode usar a configuração para armazenar valores para determinadas chaves, ou seja, o valor de ativação pode nunca ser usado.

As chaves de ativação são armazenadas internamente de maneira hierárquica semelhante às chaves do registro no Windows. Para especificar uma subchave específica, é construído um "caminho de chave" que especifica as várias chaves em um formato delimitado por barra.

Por exemplo, para ler o valor da \_ chave "ação padrão" localizada na seguinte árvore de chave:

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

A cadeia de caracteres de caminho *activationKey* seria especificada da seguinte maneira:

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

