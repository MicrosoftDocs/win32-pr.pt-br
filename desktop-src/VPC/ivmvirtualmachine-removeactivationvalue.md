---
title: Método IVMVirtualMachine RemoveActivationValue (VPCCOMInterfaces. h)
description: Remove o valor da configuração de ativação especificada para esta máquina virtual.
ms.assetid: 8e9b9d95-aec9-4b73-afc3-cd0d7300f40f
keywords:
- RemoveActivationValue do método virtual PC
- Método RemoveActivationValue Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método RemoveActivationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fcb531a405f66e39f9821e36f10d3e65e1e8b771472d87d0bce9e415dd672a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653026"
---
# <a name="ivmvirtualmachineremoveactivationvalue-method"></a>Método IVMVirtualMachine:: RemoveActivationValue

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Remove o valor da configuração de ativação especificada para esta máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RemoveActivationValue(
  [in] BSTR activationKey
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*activationKey* \[ no\]
</dt> <dd>

A chave usada para identificar o valor de ativação, como armazenado no \* arquivo ". vmc".

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                      | Descrição                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                            | A operação foi bem-sucedida.<br/>                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>           | O parâmetro é **nulo** ou está vazio.<br/>                                          |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>      | A configuração é desconhecida.<br/>                                                |
| <dl> <dt>**VM \_ E \_ pref \_ não \_ encontrado**</dt> <dt>0xA0040300</dt> </dl> | A preferência não foi encontrada ou essa configuração não tem ativação válida.<br/> |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>      | Ocorreu um erro inesperado.<br/>                                            |



 

## <a name="remarks"></a>Comentários

Esse método fornece acesso de baixo nível a qualquer valor de ativação. Ele pode ser usado para remover valores de ativação para chaves definidas pelo cliente. Tenha cuidado ao usar esse método para remover valores de ativação do sistema, já que alguns valores não podem ser alterados enquanto a máquina virtual está em execução. Quando uma máquina virtual é iniciada, uma cópia é feita de seus valores de configuração, que se torna seu conjunto de valores de ativação. Os valores de ativação são mantidos até que a máquina virtual seja desligada ou reiniciada. observe que Windows Virtual PC só pode usar a configuração para armazenar valores para determinadas chaves, ou seja, o valor de ativação pode nunca ser usado.

> [!Note]  
> A sessão da máquina virtual deve estar em execução antes que qualquer valor de ativação possa ser alterado.

 

As chaves de ativação são armazenadas internamente de maneira hierárquica semelhante às chaves do registro no Windows. Para especificar uma subchave específica, é construído um "caminho de chave" que especifica as várias chaves em um formato delimitado por barra.

Por exemplo, para remover o valor da \_ chave "ação padrão" localizada na seguinte árvore de chave:

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

 

