---
title: Os novos tipos de dados
description: Três classes de tipos de dados foram introduzidas para tipos de dados de precisão fixa do Windows de 64 bits, tipos de precisão de ponteiro e tipos de precisão de ponteiros específicos.
ms.assetid: 016977d4-e7bf-463e-9755-7ef13f16e9e5
keywords:
- Guia de programação do Windows de 64 bits, programação de Windows de bit 64, tipos de dados
- tipos de dados programação de 64 bits do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6cf5960b5344da1d459d12dee96a2f67f2cfbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294420"
---
# <a name="the-new-data-types"></a>Os novos tipos de dados

Três classes de tipos de dados foram introduzidas para janelas de 64 bits: tipos de dados de precisão fixa, tipos de precisão de ponteiro e tipos de precisão de ponteiros específicos. Esses tipos foram adicionados ao ambiente de desenvolvimento para permitir que os desenvolvedores se preparem para o Windows de 64 bits. Esses tipos são derivados do inteiro básico de linguagem C e dos tipos longos. Portanto, você pode usar esses tipos de dados no código que você compila e testa em janelas de 32 bits e, em seguida, recompilar com o compilador de 64 bits ao direcionar janelas de bits de 64.

Mesmo para aplicativos destinados apenas ao Windows de 32 bits, a adoção desses novos tipos de dados torna seu código mais robusto. Para usar esses tipos de dados, você deve verificar seu código para obter o uso de ponteiros, polimorfismo e definições de dados potencialmente inseguros. Por exemplo, quando uma variável é do tipo **ULONG \_ PTR**, fica claro que ela será usada para ponteiros de conversão para operações aritméticas ou polimorfismo. Não é possível indicar tal uso diretamente usando os tipos de dados mais antigos. (Você pode fazer isso indiretamente usando a nomenclatura de tipo derivado ou a notação húngara, mas ambas as técnicas estão sujeitas a erros.)

Todos esses tipos de dados são declarados em BaseTsd. h. Para obter mais informações, incluindo definições desses tipos de dados, consulte [tipos de dados do Windows](/windows/desktop/WinProg/windows-data-types).

## <a name="fixed-precision"></a>Precisão fixa

Os tipos de dados de precisão fixa têm o mesmo comprimento nas janelas de 32 e 64 bits. Para ajudá-lo a se lembrar disso, sua precisão é parte do nome do tipo de dados. A seguir estão os tipos de dados de precisão fixa.



| Termo                                                                       | Descrição                        |
|----------------------------------------------------------------------------|------------------------------------|
| <span id="DWORD32"></span><span id="dword32"></span>**DWORD32**<br/> | Inteiro sem sinal de 32 bits<br/> |
| <span id="DWORD64"></span><span id="dword64"></span>**DWORD64**<br/> | Inteiro sem sinal de 64 bits<br/> |
| <span id="INT32"></span><span id="int32"></span>**INT32**<br/>       | Inteiro com sinal de 32 bits<br/>   |
| <span id="INT64"></span><span id="int64"></span>**INT64**<br/>       | Inteiro com sinal de 64 bits<br/>   |
| <span id="LONG32"></span><span id="long32"></span>**LONG32**<br/>    | Inteiro com sinal de 32 bits<br/>   |
| <span id="LONG64"></span><span id="long64"></span>**LONG64**<br/>    | Inteiro com sinal de 64 bits<br/>   |
| <span id="UINT32"></span><span id="uint32"></span>**UINT32**<br/>    | **INT32** não assinado<br/>      |
| <span id="UINT64"></span><span id="uint64"></span>**UINT64**<br/>    | **Int64** não assinado<br/>      |
| <span id="ULONG32"></span><span id="ulong32"></span>**ULONG32**<br/> | **LONG32** não assinado<br/>     |
| <span id="ULONG64"></span><span id="ulong64"></span>**ULONG64**<br/> | **LONG64** não assinado<br/>     |



 

## <a name="pointer-precision"></a>Precisão do ponteiro

À medida que a precisão do ponteiro muda (ou seja, quando se torna 32 bits em janelas de 32 bits e 64 bits com o Windows de 64 bits), os tipos de dados de precisão do ponteiro refletem a precisão de acordo. Portanto, é seguro converter um ponteiro para um desses tipos ao executar aritmética de ponteiro; se a precisão do ponteiro for de 64 bits, o tipo será de 64 bits. Os tipos de contagem também refletem o tamanho máximo para o qual um ponteiro pode se referir. A seguir estão os tipos de precisão e de contagem de ponteiros.



| Termo                                                                              | Descrição                                                                                                                      |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span id="DWORD_PTR"></span><span id="dword_ptr"></span>**PTR de DWORD \_**<br/> | Tipo longo sem sinal para precisão de ponteiro.<br/>                                                                             |
| <span id="HALF_PTR"></span><span id="half_ptr"></span>**MEIO \_ PTR**<br/>    | Metade do tamanho de um ponteiro. Use em uma estrutura que contém um ponteiro e dois campos pequenos.<br/>                      |
| <span id="INT_PTR"></span><span id="int_ptr"></span>**INT \_ PTR**<br/>       | Tipo de inteiro assinado para precisão do ponteiro.<br/>                                                                            |
| <span id="LONG_PTR"></span><span id="long_ptr"></span>**\_PTR longo**<br/>    | Tipo longo assinado para precisão do ponteiro.<br/>                                                                               |
| <span id="SIZE_T"></span><span id="size_t"></span>**TAMANHO \_ T**<br/>          | O número máximo de bytes aos quais um ponteiro pode se referir. Use para uma contagem que deve abranger o intervalo completo de um ponteiro.<br/> |
| <span id="SSIZE_T"></span><span id="ssize_t"></span>**SSIZE \_ T**<br/>       | **\_ T de tamanho** assinado.<br/>                                                                                                   |
| <span id="UHALF_PTR"></span><span id="uhalf_ptr"></span>**UHALF \_ PTR**<br/> | **Meia \_ PTR** sem sinal.<br/>                                                                                               |
| <span id="UINT_PTR"></span><span id="uint_ptr"></span>**PTR-UINT \_**<br/>    | **\_ PTR de int** não assinado.<br/>                                                                                                |
| <span id="ULONG_PTR"></span><span id="ulong_ptr"></span>**\_ponteiro ULONG**<br/> | **\_ PTR Long** não assinado.<br/>                                                                                               |



 

## <a name="specific-pointer-precision-types"></a>Tipos de Pointer-Precision específicos

Os novos tipos de ponteiros a seguir redimensionam explicitamente o ponteiro. Tenha cuidado ao usar ponteiros no código de 64 bits: se você declarar o ponteiro usando um tipo de bit 32, o sistema operacional criará o ponteiro truncando um ponteiro de 64 bits. (Todos os ponteiros são 64 bits no Windows de 64 bits.)



| Termo                                                                                 | Descrição                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="POINTER_32"></span><span id="pointer_32"></span>**PONTEIRO \_ 32**<br/> | Um ponteiro de 32 bits. No Windows de 32 bits, esse é um ponteiro nativo. No Windows de 64 bits, esse é um ponteiro de bit de 64 truncado.<br/>                                                                                       |
| <span id="POINTER_64"></span><span id="pointer_64"></span>**PONTEIRO \_ 64**<br/> | Um ponteiro de 64 bits. No Windows de 64 bits, esse é um ponteiro nativo. No Windows de 32 bits, esse é um ponteiro de bit de 32 de sinal estendido. <br/> Observe que não é seguro assumir o estado do bit de ponteiro alto.<br/> |



 

 

