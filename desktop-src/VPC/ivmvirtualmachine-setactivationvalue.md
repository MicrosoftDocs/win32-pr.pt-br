---
title: Método setactivavalue IVMVirtualMachine (VPCCOMInterfaces. h)
description: Define o valor da configuração de ativação especificada para esta máquina virtual.
ms.assetid: 6d664a80-1777-42ca-8454-df84c64ab505
keywords:
- Método setactivavalue Virtual PC
- Método setactivavalue Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método setactivavalue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SetActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c7cb48b5691a9ca99a0fca5b696d8b545a40e46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455685"
---
# <a name="ivmvirtualmachinesetactivationvalue-method"></a>Método IVMVirtualMachine:: setactivationvalue

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define o valor da configuração de ativação especificada para esta máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetActivationValue(
  [in] BSTR    activationKey,
  [in] VARIANT activationValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*activationKey* \[ no\]
</dt> <dd>

A chave usada para identificar o valor de ativação, como armazenado no \* arquivo ". vmc".

</dd> <dt>

*activationvalue* \[ no\]
</dt> <dd>

O valor de ativação. Esse valor pode ser um dos seguintes tipos **variantes** : **VT \_ array** \| **VT \_ UI1** (bytes brutos), **VT \_ BSTR** (String), **VT \_ UI4** (Integer) ou **VT \_ bool** (booliano).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                      | Descrição                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                            | A operação foi bem-sucedida.<br/>                                                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>           | O parâmetro *activationKey* é **nulo** ou vazio, ou o parâmetro *activationvalue* não é um tipo de variante válido.<br/> |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>      | A configuração é desconhecida.<br/>                                                                                       |
| <dl> <dt>**VM \_ E \_ pref \_ não \_ encontrado**</dt> <dt>0xA0040300</dt> </dl> | A configuração não tem ativação válida.<br/>                                                                          |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>      | Ocorreu um erro inesperado.<br/>                                                                                   |



 

## <a name="remarks"></a>Comentários

Esse método fornece acesso de baixo nível a qualquer valor de ativação. Ele pode ser usado para definir valores de ativação para chaves definidas pelo cliente. Tenha cuidado ao usar esse método para definir valores de ativação do sistema, pois nenhuma verificação de erro é executada no valor de ativação. Além disso, alguns valores de ativação não podem ser alterados enquanto a máquina virtual está em execução. Quando uma máquina virtual é iniciada, uma cópia é feita de seus valores de configuração, que se torna seu conjunto de valores de ativação. Os valores de ativação são mantidos até que a máquina virtual seja desligada ou reiniciada. Observe que o Windows Virtual PC pode usar apenas a configuração para armazenar valores para determinadas chaves, ou seja, o valor de ativação pode nunca ser usado.

> [!Note]  
> A sessão da máquina virtual deve estar em execução antes que qualquer valor de ativação possa ser alterado.

 

As chaves de ativação são armazenadas internamente de maneira hierárquica semelhante às chaves do registro no Windows. Para especificar uma subchave específica, é construído um "caminho de chave" que especifica as várias chaves em um formato delimitado por barra.

Por exemplo, para definir o valor da \_ chave "ação padrão" localizada na seguinte árvore de chave:

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

