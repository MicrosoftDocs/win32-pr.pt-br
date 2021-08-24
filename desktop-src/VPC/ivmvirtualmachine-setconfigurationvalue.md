---
title: Método setconfigurationvalue IVMVirtualMachine (VPCCOMInterfaces. h)
description: Define o valor da definição de configuração especificada para esta VM (máquina virtual).
ms.assetid: 43c3ac88-2e25-4c9e-a2ac-fcae5add62c5
keywords:
- Método setconfigurationvalue Virtual PC
- Método setconfigurationvalue Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método setconfiguraçãovalue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7edef64484161f6151b1d2ac14fd6916a7d2a082c0c787b983019305027f4949
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652966"
---
# <a name="ivmvirtualmachinesetconfigurationvalue-method"></a>Método IVMVirtualMachine:: setconfigurationvalue

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define o valor da definição de configuração especificada para esta VM (máquina virtual).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    configurationKey,
  [in] VARIANT configurationValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*configurationKey* \[ no\]
</dt> <dd>

A chave usada para identificar o valor de configuração como armazenado no \* arquivo ". vmc".

> [!IMPORTANT]
> As alterações devem ser feitas em " \* . vmc" usando apenas  o método setconfigurevalue. \*Não há suporte para alterar ". vmc" usando qualquer outro método.

 

</dd> <dt>

*configuração* \[ no\]
</dt> <dd>

O valor de configuração. Esse valor Cay ser um dos seguintes tipos **variantes** : **VT \_ array** \| **VT \_ UI1** (bytes brutos), **VT \_ BSTR** (String), **VT \_ UI4** (Integer) ou **VT \_ bool** (booliano).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                 | Descrição                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>      | O parâmetro *configurationKey* é **nulo** ou vazio ou o parâmetro *ConfigurationValue* não é um tipo Variant válido.<br/> |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl> | A configuração é desconhecida.<br/>                                                                                            |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/>                                                                                        |



 

## <a name="remarks"></a>Comentários

Os valores a seguir têm suporte para o parâmetro *configurationKey* .



| valor de *configurationKey*                                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Tipo de dados            | Valor padrão     |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-------------------|
| "sincronização de hardware/BIOS/horário \_ \_ na \_ inicialização"<br/>              | "true" se o relógio CMOS da VM for sincronizado com o relógio do host na inicialização; caso contrário, "false".<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | Boolean<br/> | "true"<br/> |
| "integração/Microsoft/sincronização de horário do host \_ \_ /habilitado" "<br/> | "verdadeiro" se a sincronização de tempo do host estiver habilitada nos componentes de integração; caso contrário, "false".<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Boolean<br/> | "true"<br/> |
| "opções da interface do usuário \_ /publicação automática de \_ aplicativo \_ "<br/>                  | "verdadeiro" se a publicação automática de aplicativos estiver habilitada nos componentes de integração; caso contrário, "false". Isso também é chamado de aplicativos virtuais.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Boolean<br/> | "true"<br/> |
| "opções de interface do usuário \_ /segundos \_ para \_ salvar"<br/>                   | Número de segundos a aguardar antes de salvar a VM depois que todos os aplicativos forem fechados. No entanto, os valores abaixo de 20 e mais de 4.294.968 têm significados especiais. Para obter detalhes, consulte a lista a seguir<br/> <dl> <dt><span id="0"></span>0</dt> <dd> Nunca salve a VM.<br/> </dd> <dt><span id="120"></span>1 20</dt> <dd> Aguarde 20 segundos antes de salvar a VM.<br/> </dd> <dt><span id="214_294_967"></span>21 4.294.967</dt> <dd> Aguarde o número especificado de segundos antes de salvar a VM.<br/> </dd> <dt><span id="4_294_9684_294_967_295"></span>4.294.968 4.294.967.295</dt> <dd> Aguarde 4.294.968 segundos antes de salvar a VM.<br/> </dd> </dl> | valores<br/> | 300<br/>    |



 

Esse método fornece acesso de baixo nível a qualquer valor de configuração. Ele pode ser usado para definir valores de configuração para chaves definidas pelo cliente. Tenha cuidado se você usar esse método para definir valores de configuração do sistema, porque nenhuma verificação de erro é executada no valor de configuração. Além disso, alguns valores de configuração não podem ser alterados enquanto a máquina virtual está em execução.

As chaves de configuração estão localizadas no arquivo " \* . vmc" da máquina virtual no formato XML. As chaves são armazenadas de maneira hierárquica semelhante às chaves do registro no Windows. Para especificar uma subchave específica, é construído um "caminho de chave" que especifica as várias chaves em um formato delimitado por barra.

Por exemplo, para definir o valor da chave "tamanho da RAM \_ " localizado na seguinte árvore de chave:

``` syntax
<preferences>
  <hardware>
    <bios>
      <time_sync_at_boot type="boolean">true</time_sync_at_boot>
```

A cadeia de caracteres de caminho *configurationKey* seria especificada da seguinte maneira:

``` syntax
"hardware/memory/ram_size"
```

Se qualquer uma das chaves na árvore desejada tiver um valor de atributo "ID", o atributo e seu valor serão inseridos na cadeia de caracteres de caminho *configurationKey* imediatamente após sua chave de configuração associada usando o seguinte formato entre colchetes: " \[ @id ="*\_ valor de ID*" \] ".

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

A cadeia de caracteres de caminho *configurationKey* seria especificada da seguinte maneira:

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
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
</dt> <dt>

[**IVMVirtualPC:: setconfigurationvalue**](ivmvirtualpc-setconfigurationvalue.md)
</dt> </dl>

 

