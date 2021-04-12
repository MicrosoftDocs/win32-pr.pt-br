---
title: Método setconfigurationvalue IVMVirtualPC (VPCCOMInterfaces. h)
description: Define o valor da definição de configuração especificada.
ms.assetid: 7760b81e-734d-4970-8875-f2d310ff6c5c
keywords:
- Método setconfigurationvalue Virtual PC
- Método setconfigurationvalue Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método setconfiguraçãovalue
topic_type:
- apiref
api_name:
- IVMVirtualPC.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecb8ff3bb68829e944461cedb1c86904c7150593
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499604"
---
# <a name="ivmvirtualpcsetconfigurationvalue-method"></a>Método IVMVirtualPC:: setconfigurationvalue

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define o valor da definição de configuração especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    preferenceKey,
  [in] VARIANT preferenceValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*preferenceKey* \[ no\]
</dt> <dd>

A chave usada para identificar a preferência, conforme armazenado no arquivo de configuração por usuário (Options.xml em "% LocalAppData% \\ Microsoft \\ Windows Virtual PC").

> [!IMPORTANT]
> As alterações devem ser feitas para Options.xml apenas usando **o método** setconfigurevalue. Não há suporte para a alteração de Options.xml usando qualquer outro método.

 

</dd> <dt>

*preferência* \[ no\]
</dt> <dd>

O valor de preferência. Esse valor pode ser um dos seguintes tipos **variantes** : **VT \_ array** \| **VT \_ UI1** (bytes brutos), **VT \_ BSTR** (String), **VT \_ UI4** (Integer) ou **VT \_ bool** (booliano).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                        | Descrição                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | A operação foi bem-sucedida.<br/>                                                        |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                                | O parâmetro *preferenceKey* ou *preferencevalue* é **nulo**.<br/>                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                             | O parâmetro *preferenceKey* não é válido ou é uma cadeia de caracteres vazia.<br/>                    |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                        | Ocorreu um erro inesperado.<br/>                                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> <dt>0x80070005</dt> </dl>                           | O usuário atual não tem acesso suficiente ao arquivo de configuração.<br/>                  |
| <dl> <dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt> </dl> | O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).<br/> |



 

## <a name="remarks"></a>Comentários

Os valores a seguir têm suporte para o parâmetro *preferenceKey* .



| valor de *preferenceKey*      | Descrição                                                                                                                                                                           | Tipo de dados            | Valor padrão   |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-----------------|
| " \_ tempo limite de ociosidade"<br/> | Número de segundos que vpc.exe deve aguardar antes de sair se não houver VMs ou aplicativos ativos usando as [interfaces do Windows Virtual PC](virtual-pc-interfaces.md).<br/> | valores<br/> | máximo<br/> |



 

Esse método fornece acesso de baixo nível a qualquer valor de configuração. Ele pode ser usado para definir valores de configuração para chaves definidas pelo cliente. Tenha cuidado se você usar esse método para definir valores de configuração do sistema, porque nenhuma verificação de erro é executada no valor de configuração. Além disso, alguns valores de configuração não podem ser alterados enquanto uma máquina virtual está em execução.

As chaves de configuração estão localizadas no arquivo "Options.xml" da máquina virtual no formato XML. As chaves são armazenadas de maneira hierárquica semelhante às chaves do registro no Windows. Para especificar uma subchave específica, é construído um "caminho de chave" que especifica as várias chaves em um formato delimitado por barra.

Por exemplo, para definir o valor da \_ chave "tempo limite de ociosidade" localizado na seguinte árvore de chave:

``` syntax
<preferences>
  <idle_timeout type="integer">60</idle_timeout>
```

A cadeia de caracteres de caminho *preferenceKey* seria especificada da seguinte maneira:

``` syntax
"idle_timeout"
```

Se qualquer uma das chaves na árvore desejada tiver um valor de atributo "ID", o atributo e seu valor serão inseridos na cadeia de caracteres de caminho *preferenceKey* imediatamente após sua chave de configuração associada usando o seguinte formato entre colchetes: " \[ @id ="*\_ valor de ID*" \] ".

Por exemplo, para definir o valor da chave "golfe" localizada na seguinte árvore de chave:

``` syntax
<preferences>
  <alpha>
    <bravo>
      <charlie>
        <delta id="1">
          <echo id="0">
            <foxtrot>
              <golf type="string">D</golf>
```

A cadeia de caracteres de caminho *preferenceKey* seria especificada da seguinte maneira:

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> <dt>

[**IVMVirtualMachine:: setconfigurationvalue**](ivmvirtualmachine-setconfigurationvalue.md)
</dt> </dl>

 

