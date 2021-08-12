---
title: Método getconfigurationvalue IVMVirtualMachine (VPCCOMInterfaces. h)
description: Recupera o valor da definição de configuração especificada para esta máquina virtual.
ms.assetid: fd3c509e-8a40-4828-b866-6bd2cb455ab2
keywords:
- PC virtual do método getconfigurationvalue
- Método getconfigurationvalue Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método getconfigurationvalue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b58a048b2dd93f6aab7f071912519dac356896d6e32a13809f4560a3db9fb8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592711"
---
# <a name="ivmvirtualmachinegetconfigurationvalue-method"></a>Método IVMVirtualMachine:: getconfigurationvalue

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o valor da definição de configuração especificada para esta máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    configurationKey,
  [out, retval] VARIANT *configurationValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*configurationKey* \[ no\]
</dt> <dd>

A chave usada para identificar o valor de configuração como armazenado no \* arquivo ". vmc".

</dd> <dt>

*configuração* \[ out, retval\]
</dt> <dd>

O valor de configuração. Esse valor pode ser um dos seguintes tipos **variantes** : **VT \_ array** \| **VT \_ UI1** (bytes brutos), **VT \_ BSTR** (String), **VT \_ i4** (Integer) ou **VT \_ bool** (booliano).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                      | Descrição                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                            | A operação foi bem-sucedida.<br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>           | O parâmetro *configurationKey* é **nulo** ou está vazio.<br/> |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>              | O parâmetro *ConfigurationValue* é **nulo**.<br/>        |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>      | A configuração é desconhecida.<br/>                          |
| <dl> <dt>**VM \_ E \_ pref \_ não \_ encontrado**</dt> <dt>0xA0040300</dt> </dl> | A preferência não foi encontrada.<br/>                          |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>      | Ocorreu um erro inesperado.<br/>                      |



 

## <a name="remarks"></a>Comentários

Esse método fornece acesso de baixo nível a qualquer valor de configuração. Ele pode ser usado para ler valores de configuração para chaves definidas pelo cliente.

As chaves de configuração estão localizadas no arquivo " \* . vmc" da máquina virtual no formato XML. As chaves são armazenadas de maneira hierárquica semelhante às chaves do registro no Windows. Para especificar uma subchave específica, é construído um "caminho de chave" que especifica as várias chaves em um formato delimitado por barra.

Por exemplo, para ler o valor da chave "tamanho da RAM \_ " localizada na seguinte árvore de chave:

``` syntax
<hardware>
    <memory>
        <ram_size type="integer">128</ram_size>
```

A cadeia de caracteres de caminho *configurationKey* seria especificada da seguinte maneira:

``` syntax
"hardware/memory/ram_size"
```

Se qualquer uma das chaves na árvore desejada tiver um valor de atributo "ID", o atributo e seu valor serão inseridos na cadeia de caracteres de caminho *configurationKey* imediatamente após sua chave de configuração associada usando o seguinte formato entre colchetes: " \[ @id ="*\_ valor de ID*" \] ".

Por exemplo, para ler o valor da chave "Absolute" localizada na seguinte árvore de chave:

``` syntax
<hardware>
    <pci_bus>
        <ide_adapter>
            <ide_controller id="1">
                <location id="0">
                    <pathname>
                        <absolute type="string">D</absolute>
```

A cadeia de caracteres de caminho *configurationKey* seria especificada da seguinte maneira:

``` syntax
"hardware/pci_bus/ide_adapter/ide_controller[@id=1]/location[@id=0]/pathname/absolute"
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

